# Use the official JBoss Keycloak image as the base image
FROM jboss/keycloak

# Set the working directory to the Keycloak deployment directory
WORKDIR /opt/jboss/keycloak/standalone/deployments/

# Copy your JAR file to the deployment directory
COPY ./target/admin-server.jar

# Optional: If you have any additional configuration files, you can copy them here
# COPY config/your-config-file.xml /opt/jboss/keycloak/standalone/configuration/

# Start Keycloak
CMD ["./start-keycloak.sh"]
