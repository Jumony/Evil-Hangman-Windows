CC = gcc
CFLAGS = -g -Wall -std=c99
OBJECTS = main.o my_string.o generic_vector.o avl_tree.o hangman.o
TEST_OBJECTS = unit_test.o test_def.o my_string.o
HEADERS = hangman.h

string_driver.exe: $(OBJECTS)
	$(CC) $(CFLAGS) -o string_driver.exe $(OBJECTS)

main.o: main.c
	$(CC) $(CFLAGS) -c main.c -o main.o

my_string.o: my_string.c
	$(CC) $(CFLAGS) -c my_string.c -o my_string.o

generic_vector.o: generic_vector.c
	$(CC) $(CFLAGS) -c generic_vector.c -o generic_vector.o

avl_tree.o: avl_tree.c
	$(CC) $(CFLAGS) -c avl_tree.c -o avl_tree.o

hangman.o: hangman.c $(HEADERS)
	$(CC) $(CFLAGS) -c hangman.c -o hangman.o

unit_test.exe: my_string.o unit_test.o test_def.o
	$(CC) $(CFLAGS) -o unit_test.exe unit_test.o test_def.o my_string.o

unit_test.o: unit_test.c
	$(CC) $(CFLAGS) -c unit_test.c -o unit_test.o

test_def.o: test_def.c
	$(CC) $(CFLAGS) -c test_def.c -o test_def.o

clean:
	rm string_driver.exe unit_test.exe $(OBJECTS) $(TEST_OBJECTS)
