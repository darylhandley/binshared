# start up iq
cd insight-brain-service && 
mvn exec:java -Dexec.mainClass=com.sonatype.insight.brain.service.InsightBrainService -Dexec.args='server src/test/resources/config-dev.yml'
