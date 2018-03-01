CC=gcc
RM=rm -f

all : build archive doc

archive : collegemain.cc node.h tarray.h myexe course.cc course.h college.cc college.h
	tar -cvzf college.tar.gz node.h tarray.h myexe course.cc course.h collegemain.cc college.cc college.h
	
build : collegemain.o course.o college.o
	g++ -g -o myexe collegemain.o course.o college.o
	
doc : node.h tarray.h myexe course.cc course.h collegemain.cc college.cc college.h

collegemain.o : collegemain.cc node.h tarray.h

college.o : college.h college.cc

course.o : course.h course.cc

clean : 
	$(RM) myexe collegemain.o course.o college.o