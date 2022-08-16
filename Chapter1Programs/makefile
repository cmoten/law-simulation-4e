# define the compliler to use
CC = gcc

#define the compiler flags
CFLAGS = -std=c11 -Wall -ferror-limit=10 -Wextra -target arm64-apple-darwin

#define the library paths in addition to /usr/lib
LFLAGS = -l

#define libraries to use
LIBS = m

#define the object files this project needs
OBJFILES = mm1-10.o lcgrand.o

#define the name of the executable file
MAIN = program

#define output files
OUTPUT = mm1-10.out

#all of the below is generic  - one only typically adjusts the above

all: $(MAIN)

$(MAIN): $(OBJFILES)
	$(CC) $(CFLAGS) -o $(MAIN) $(OBJFILES) $(LFLAGS)$(LIBS)

%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $< 

clean:
	rm -f $(OBJFILES) $(MAIN) $(OUTPUT)

