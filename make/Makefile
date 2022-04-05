SRC = ./../src/
OBJ = ./../obj/
BIN = ./../bin/
GFLAGS = g++
INC = ./../include/
CFLAGS = -c -g -Wall
OFLAGS = -lm -o
IFLAGS = -I./../include/
EXECS = $(BIN)final


$(BIN)final :$(OBJ)main.o $(OBJ)Loan.o $(OBJ)Farmer.o $(OBJ)Address.o
	$(GFLAGS) $(OFLAGS)final $(OBJ)main.o $(OBJ)Loan.o $(OBJ)Farmer.o $(OBJ)Address.o
	mv final $(BIN)

$(OBJ)main.o:$(SRC)main.cpp $(INC)header.h 
	$(GFLAGS) $(CFLAGS) $(SRC)main.cpp $(IFLAGS)
	mv main.o $(OBJ)

$(OBJ)Loan.o:$(SRC)Loan.cpp $(INC)header.h $(INC)loan.h
	$(GFLAGS) $(CFLAGS) $(SRC)Loan.cpp $(IFLAGS)
	mv Loan.o $(OBJ)

$(OBJ)Farmer.o:$(SRC)Farmer.cpp $(INC)header.h $(INC)loan.h
	$(GFLAGS) $(CFLAGS) $(SRC)Farmer.cpp $(IFLAGS)
	mv Farmer.o $(OBJ)

$(OBJ)Address.o:$(SRC)Address.cpp $(INC)header.h
	$(GFLAGS) $(CFLAGS) $(SRC)Address.cpp $(IFLAGS)
	mv Address.o $(OBJ)

clean:
	rm $(OBJ)*
	rm $(BIN)final

valgrind:$(EXECS)
	valgrind $(VFLAGS) $(BIN)final
