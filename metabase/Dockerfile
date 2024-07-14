FROM metabase/metabase-enterprise:v1.50.10

# Copy log4j2.xml into the image
COPY log4j2.xml /etc/metabase/log4j2.xml

# Set JAVA_OPTS environment variables here
ENV JAVA_OPTS="-Dlog4j.configurationFile=file:/etc/metabase/log4j2.xml"
