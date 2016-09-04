FROM 1science/java:oracle-jre-8
ENV UPDATE 10000
ENV ARTHUR arthur
ENV JAR knight.jar
ENV URL http://gp.powertrip.pt/build/artifacts/
ENV AHOST arthur
ENV APORT 8080
CMD wget ${URL}${JAR} && java -jar ${JAR} http://${AHOST}:${APORT} ${UPDATE}
