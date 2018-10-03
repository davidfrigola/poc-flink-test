# POC - Testing flink apps

Currently at work there's a team developing flinks apps, but testing is only in integration.
I'd like to be able to do some unit tests as `Integration` ones, spinning up Flink app and doing an e2e testing every build (even local)


# The app

Simple app with the following specification:
* Stream application 
* Reading from Kafka topic
* Simple logic (add a prefix/suffix?) applied to the stream elements
* POST the result to :
** a third-party system (REST service)
** a Kafka topic

# Goals

Integration tests should:
* GIVEN Set data to be streamed via Kafka - write the initial data
* WHEN - flink app is started
* THEN - REST service is hit with a POST, modified data

# Initial tools to use

* JUnit 5
* Kafka - spin up a docker container/java code?
* Wiremock as REST service - see Vefiry feature

# Lessons learnt

* TODO : add any lessons learn in the way
