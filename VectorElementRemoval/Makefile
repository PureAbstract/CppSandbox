include ../compilerSettings_clang3.5.mk

SOURCES=VectorElementRemoval.cpp
EXECUTABLE=VectorElementRemoval

OBJECTS=$(SOURCES:.cpp=.o)

run: binaries
	time ./CheckValues
	time ./RemoveValues

binaries: $(SOURCES)
	${CC} ${CFLAGS} ${LDFLAGS} VectorElementRemoval.cpp -DCHECK_VALUES -o CheckValues
	${CC} ${CFLAGS} ${LDFLAGS} VectorElementRemoval.cpp -DREMOVE_VALUES -o RemoveValues

edit:
	vim $(SOURCES)

clean:
	- rm ./CheckValues ./RemoveValues

.PHONY: clean

