
# clean build 
mvn clean install -T 1C -DskipTests

# general build - after pull 
mvn install -T 1C -DskipTests 

# incremental compile - note that sonatype-nexus-repository 
# is always needed or the jar won't get rebuilt
mvn install -pl :nexus-common,:sonatype-nexus-repository

