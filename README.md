# xqa-ingest-balancer [![Build Status](https://travis-ci.org/jameshnsears/xqa-ingest-balancer.svg?branch=master)](https://travis-ci.org/jameshnsears/xqa-ingest-balancer) [![Coverage Status](https://coveralls.io/repos/github/jameshnsears/xqa-ingest-balancer/badge.svg?branch=master)](https://coveralls.io/github/jameshnsears/xqa-ingest-balancer?branch=master) [![sonarcloud.io](https://sonarcloud.io/api/project_badges/measure?project=jameshnsears_xqa-ingest-balancer&metric=alert_status)](https://sonarcloud.io/dashboard?id=jameshnsears_xqa-ingest-balancer) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/d2624e3cf96045fcb31003094b591fc3)](https://www.codacy.com/app/jameshnsears/xqa-ingest-balancer?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=jameshnsears/xqa-ingest-balancer&amp;utm_campaign=Badge_Grade)
* distributes XML across XQA BaseX engine(s).

## 1. High Level Design
![High Level Design](uml/xqa-ingest-balancer.jpg)

## 2. Build
* ./build.sh

## 3. Bring up
* docker-compose up -d xqa-message-broker

## 4. Test

### 4.1. Maven
* mvn clean compile test
* mvn jacoco:report coveralls:report
* mvn site  # findbugs

### 4.2. CLI
* java -jar target/xqa-ingest-balancer-1.0.0-SNAPSHOT-jar-with-dependencies.jar -message_broker_host 127.0.0.1 -pool_size 4

or

* POOL_SIZE=4 docker-compose up -d

## 5. Teardown
* docker-compose down -v
