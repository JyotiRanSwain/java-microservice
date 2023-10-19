# Use the official JBoss Keycloak image as the base image
FROM jboss/keycloak

# Set the working directory to the Keycloak deployment directory
WORKDIR /opt/jboss/keycloak/standalone/deployments/

# Copy your JAR file to the deployment directory
COPY ./target/admin-server.jar /opt/jboss/keycloak/standalone/deployments/

# Start Keycloak
CMD ["./start-keycloak.sh"]
