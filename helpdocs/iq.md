
# do a clean build
mvn install -DskipTests -Dskip-obfuscate  -Dcheckstyle.skip=true  -Dpmd.skip=true

# rebuild the other stuff
cd insight-brain-data && mvn clean install -DskipTests && cd ..


# start up iq
cd insight-brain-service && 
mvn exec:java -Dexec.mainClass=com.sonatype.insight.brain.service.InsightBrainService -Dexec.args='server src/test/resources/config-dev.yml'
