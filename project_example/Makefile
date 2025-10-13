OUT ?= project

OUT_DBG := $(OUT)_debug
OUT_REL := $(OUT)

ifeq ($(OS), Windows_NT)
	OUT_DBG := $(OUT_DBG).exe
	OUT_REL := $(OUT_REL).exe
endif

CXX := g++

CXXFLAGS ?= -Wall -std=c++17
CXXFLAGS_DBG := $(CXXFLAGS) -O0 -g -DDEBUG
CXXFLAGS_REL := $(CXXFLAGS) -O3 -DNDEBUG


SRC_DIR  := src
SRCS_C   := $(wildcard $(SRC_DIR)/*.c) $(wildcard $(SRC_DIR)/**/*.c)
SRCS_CPP := $(wildcard $(SRC_DIR)/*.cpp) $(wildcard $(SRC_DIR)/**/*.cpp)
SRCS     := $(SRCS_C) $(SRCS_CPP)


OBJ_DIR      := obj

OBJS_DBG_C   := $(patsubst $(SRC_DIR)/%.c, $(OBJ_DIR)/debug/%.o, $(SRCS_C))
OBJS_DBG_CPP := $(patsubst $(SRC_DIR)/%.cpp, $(OBJ_DIR)/debug/%.o, $(SRCS_CPP))
OBJS_DBG     := $(OBJS_DBG_C) $(OBJS_DBG_CPP)

OBJS_REL_C   := $(patsubst $(SRC_DIR)/%.c, $(OBJ_DIR)/release/%.o, $(SRCS_C))
OBJS_REL_CPP := $(patsubst $(SRC_DIR)/%.cpp, $(OBJ_DIR)/release/%.o, $(SRCS_CPP))
OBJS_REL     := $(OBJS_REL_C) $(OBJS_REL_CPP)

default: release

clean:
	rm -rf $(OBJ_DIR) $(OUT_DBG) $(OUT_REL)

# Debug definitions
debug: $(OUT_DBG)

$(OUT_DBG): $(OBJS_DBG)
	$(CXX) $(CXXFLAGS_DBG) $^ -o $@

$(OBJ_DIR)/debug/%.o: $(SRC_DIR)/%.c
	@mkdir -p $(dir $@)
	$(CXX) $(CXXFLAGS_DBG) -I$(SRC_DIR) -c $< -o $@

$(OBJ_DIR)/debug/%.o: $(SRC_DIR)/%.cpp
	@mkdir -p $(dir $@)
	$(CXX) $(CXXFLAGS_DBG) -I$(SRC_DIR) -c $< -o $@

# Release definitions
release: $(OUT_REL)

$(OUT_REL): $(OBJS_REL)
	$(CXX) $(CXXFLAGS_REL) $^ -o $@

$(OBJ_DIR)/release/%.o: $(SRC_DIR)/%.c
	@mkdir -p $(dir $@)
	$(CXX) $(CXXFLAGS_REL) -I$(SRC_DIR) -c $< -o $@

$(OBJ_DIR)/release/%.o: $(SRC_DIR)/%.cpp
	@mkdir -p $(dir $@)
	$(CXX) $(CXXFLAGS_REL) -I$(SRC_DIR) -c $< -o $@

.PHONY: clean
.PRECIOUS: $(OUT_DBG) $(OUT_REL) $(OBJS_DBG) $(OBJS_REL)
