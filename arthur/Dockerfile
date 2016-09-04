FROM 1science/java:oracle-jre-8
EXPOSE 8080
ENV JAR arthur.jar
ENV URL http://gp.powertrip.pt/build/artifacts/
ENV RPORT 6379
ENV RHOST redis
CMD wget ${URL}config.yml && \
sed -i 's/^redisPort: 22637*/redisPort: 6379/' config.yml && \
sed -i 's/^redisHost: slimecraft.pt*/redisHost: redis/' config.yml && \
wget ${URL}${JAR} && cat config.yml && java -jar arthur.jar server config.yml
