OUT ?= $(notdir $(CURDIR))
ifeq ($(OS), Windows_NT)
	OUT_EXT ?= .exe
else
	OUT_EXT ?=
endif

CXXFLAGS ?= -Wall -O3 -std=c++17

CXX := g++

SRC_DIR  := src
SRCS_C   := $(wildcard $(SRC_DIR)/*.c)
SRCS_CPP := $(wildcard $(SRC_DIR)/*.cpp)
SRCS     := $(SRCS_C) $(SRCS_CPP)

OBJ_DIR  := obj
OBJS_C   := $(patsubst $(SRC_DIR)/%.c, $(OBJ_DIR)/%.o, $(SRCS_C))
OBJS_CPP := $(patsubst $(SRC_DIR)/%.cpp, $(OBJ_DIR)/%.o, $(SRCS_CPP))
OBJS     := $(OBJS_C) $(OBJS_CPP)

default: all

clean:
	rm -rf $(OBJ_DIR) $(OUT)$(OUT_EXT)

all: $(OUT)$(OUT_EXT)

./$(OUT)$(OUT_EXT): $(OBJS)
	$(CXX) $(CXXFLAGS) $^ -o $@
	
$(OBJ_DIR)/%.o: $(SRC_DIR)/%.c $(OBJ_DIR)
	$(CXX) $(CXXFLAGS) -I$(SRC_DIR) -c $< -o $@
	
$(OBJ_DIR)/%.o: $(SRC_DIR)/%.cpp $(OBJ_DIR)
	$(CXX) $(CXXFLAGS) -I$(SRC_DIR) -c $< -o $@
	
$(OBJ_DIR):
	mkdir $(OBJ_DIR)

.PHONY: all clean
.PRECIOUS: ./%$(OUT_EXT) $(OBJ_DIR)/%.o
