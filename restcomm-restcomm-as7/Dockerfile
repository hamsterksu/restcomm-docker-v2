FROM restcomm/base:as7

MAINTAINER George Vagenas - gvagenas@telestax.com
MAINTAINER Jean Deruelle - jean.deruelle@telestax.com
MAINTAINER Lefteris Banos - liblefty@telestax.com

# download restcomm-sip-servlets
ENV install_dir /opt/Restcomm-JBoss-AS7

RUN wget -qO- https://mobicents.ci.cloudbees.com/view/RestComm/job/RestComm/lastSuccessfulBuild/artifact/restcomm-version.txt -O version.txt && mv version.txt /tmp/version && \
  wget -qc https://mobicents.ci.cloudbees.com/view/RestComm/job/RestComm/lastSuccessfulBuild/artifact/Restcomm-JBoss-AS7-`cat /tmp/version`.zip -O Restcomm-JBoss-AS7.zip && \
  unzip -qq Restcomm-JBoss-AS7.zip -d /tmp/ && \
  mv /tmp/Restcomm-JBoss-AS7-*/standalone/deployments/restcomm.war ${install_dir}/standalone/deployments/restcomm.war && \
  mv /tmp/Restcomm-JBoss-AS7-*/standalone/deployments/restcomm.war.dodeploy ${install_dir}/standalone/deployments/restcomm.war.dodeploy && \
  mv /tmp/Restcomm-JBoss-AS7-*/standalone/deployments/restcomm-management.war ${install_dir}/standalone/deployments/restcomm-management.war && \
  mv /tmp/Restcomm-JBoss-AS7-*/standalone/deployments/restcomm-management.war.dodeploy ${install_dir}/standalone/deployments/restcomm-management.war.dodeploy && \
  rm -rf /tmp/Restcomm-JBoss-AS7-* && \
  rm Restcomm-JBoss-AS7.zip

EXPOSE 5080/udp  5080/tcp 5081/tcp 5082/tcp 5083/tcp 8080/tcp 8443/tcp 5060/udp 5060/tcp 5061/tcp 5062/tcp 5063/tcp 80/tcp 443/tcp 9990/tcp