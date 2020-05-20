# Use jmeter-base as the foundation
FROM mhdrameez/jsample

MAINTAINER mhdrameez

# Create mount point for script, data and log files
VOLUME ["/scripts"]
VOLUME ["/input_data"]
VOLUME ["/logs"]

# Use a predefined configuration.  This sets the contract for connecting to jmeter servers.
ADD jmeter.properties /var/lib/apache-jmeter-5.3/bin
ADD test_google.jmx /var/lib/apache-jmeter-5.3/bin

ENTRYPOINT [ "/var/lib/apache-jmeter-5.3/bin/jmeter"]