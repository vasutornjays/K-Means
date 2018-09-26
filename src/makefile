# makkefile begins
# define a variable for compiler flags (JFLAGS)
# define a variable for the compiler (JC)  
# define a variable for the Java Virtual Machine (JVM)

ccend=$(echo -e "\033[0m")

JFLAGS = -cp
JC = javac
JVM= java 
FILE=

KMeans: KMeans.class
	jar cvf Kmean.jar KMeans.class KMeans\$$Map.class KMeans\$$Reduce.class
	@make clean
	@echo !!!!!!! Build Success !!!!!!!!

KMeans.class: KMeans.java
	$(JC) KMeans.java $(JFLAGS) /usr/local/hadoop/etc/hadoop:/usr/local/hadoop/share/hadoop/common/lib/*:/usr/local/hadoop/share/hadoop/common/*:/usr/local/hadoop/share/hadoop/hdfs:/usr/local/hadoop/share/hadoop/hdfs/lib/*:/usr/local/hadoop/share/hadoop/hdfs/*:/usr/local/hadoop/share/hadoop/mapreduce/lib/*:/usr/local/hadoop/share/hadoop/mapreduce/*:/usr/local/hadoop/share/hadoop/yarn:/usr/local/hadoop/share/hadoop/yarn/lib/*:/usr/local/hadoop/share/hadoop/yarn/*

.PHONY: clean
clean:
	@$(RM) *.class
