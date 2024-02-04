# Makefile for main
# Y. Liow
#------------------------------------------------------------------------------
# Macros
#------------------------------------------------------------------------------
CXX       = g++
CXXFLAGS  = -c -std=c++2a -fmax-errors=3 -Wall -Werror -Wextra -Wpedantic \
	    -Wconversion
OBJS      = main.o
EXE       = main.exe
#------------------------------------------------------------------------------
# Executable
#------------------------------------------------------------------------------
$(EXE):	*.cpp # add "*.h" here if necessary
	$(CXX) *.cpp -o $(EXE) $(CXXFLAGS) -g -fsanitize=address
#------------------------------------------------------------------------------
# Utilities
#------------------------------------------------------------------------------
clean:
	rm -f $(OBJS) $(EXE)
c:
	rm -f $(OBJS) $(EXE)
run:
	ASAN_OPTIONS=detect_leaks=1 ./$(EXE)
r:
	ASAN_OPTIONS=detect_leaks=1 ./$(EXE)
