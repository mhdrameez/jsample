# Use jmeter-base as the foundation
FROM mhdrameez/jsample

MAINTAINER mhdrameez

# Use a predefined configuration.  This sets the contract for connecting to jmeter servers.
ADD jmeter.properties /var/lib/apache-jmeter-5.3/bin
ADD test_google.jmx /var/lib/apache-jmeter-5.3/bin

# Expose access to logs & data files
VOLUME [ "/logs" ]
VOLUME [ "/input-data" ]

# Expose jmeter-server's port (values dicated by those specified in jmeter.properties.
EXPOSE 1099 60000

# Run jmeter-server 
ENTRYPOINT [ "/var/lib/apache-jmeter-5.3/bin/jmeter-server" ]
