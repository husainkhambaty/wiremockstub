## Wiremock Stub
An example on how to setup a quick wiremock stub for performance testing. I will be using this as a test stub service for other git projects.

This example uses the standalone jar file to quickly pick a configuration file that bring up the stub service on the designated port.

For more information please read [Getting Started](http://wiremock.org/docs/getting-started "Getting Started").

### Pre-requisites

You can download the standalone jar [here](http://repo1.maven.org/maven2/com/github/tomakehurst/wiremock-standalone/2.27.2/wiremock-standalone-2.27.2.jar "here"). Once downloaded, you should copy the jar in a safe location with the required permissions.


### Start your engines

To start the wiremock
```bash
java -jar <wiremock-jar-full-path> --port <port> --root-dir <your-mappings-path>
```

*Hint*: It is quite convenient to copy the jar to a specific location to help with standardisation such as `/opt/wiremock/bin` and use environment variables.

Example:
```bash
export WIREMOCK_PATH="/opt/wiremock"
java -jar ${WIREMOCK_PATH}/bin/wiremock-standalone-2.27.2.jar --port 8999 --root-dir ${WIREMOCK_PATH}/config/test-service --container-threads 100
```
