
all: sisctrl

CXXFLAGS=-g
LDFLAGS=-lyaml-cpp

INVOICE_OBJECTS=sisctrl.o automata.o

sisctrl: $(INVOICE_OBJECTS)
	$(CXX) -o $@ $(INVOICE_OBJECTS) $(LDFLAGS) -pthread -lpthread -lrt

sisctrl.o: sisctrl.C
	$(CXX) $(CXXFLAGS) -c $<

automata.o: automata.C automata.h
	$(CXX) $(CXXFLAGS) -c $<

clean:
	rm -f *.o *.C~ Makefile~
