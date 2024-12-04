# Усложненный make-file с переменными для параметров компиляции и исполняемых файлов

.PHONY: all debug release clean

# Переменные для флагов компиляции
RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall

# Переменные для исполняемых файлов
RELEASE_EXEC  = hello
DEBUG_EXEC    = hello-dbg

# Переменная для исходного файла
SRC = hello.cpp

all: debug release

# Цель для отладочной сборки
debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(SRC)
	g++ $(DEBUG_FLAGS) $(SRC) -o $(DEBUG_EXEC)

# Цель для релизной сборки
release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(SRC)
	g++ $(RELEASE_FLAGS) $(SRC) -o $(RELEASE_EXEC)

# Цель для очистки
clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)

