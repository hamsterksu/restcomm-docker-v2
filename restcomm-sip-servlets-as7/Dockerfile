FROM restcomm/baseimage:java7

MAINTAINER George Vagenas - gvagenas@telestax.com
MAINTAINER Jean Deruelle - jean.deruelle@telestax.com
MAINTAINER Lefteris Banos - liblefty@telestax.com

# download restcomm-sip-servlets
ENV install_dir /opt/restcomm-sip-servlets-jboss-as7

RUN wget -qO- https://mobicents.ci.cloudbees.com/view/SIP%20Servlets/job/RestcommSipServlets-Release/lastSuccessfulBuild/artifact/restcomm-sip-servlets-version.txt -O version.txt && mv version.txt /tmp/version 

RUN wget -qc https://mobicents.ci.cloudbees.com/view/SIP%20Servlets/job/RestcommSipServlets-Release/lastSuccessfulBuild/artifact/restcomm-sip-servlets-`cat /tmp/version`-jboss-as-7.2.0.Final.zip -O restcomm-sip-servlets-jboss-as7.zip 

RUN unzip restcomm-sip-servlets-jboss-as7.zip -d /opt/ && mv /opt/restcomm-sip-servlets-*/ ${install_dir} && \
rm restcomm-sip-servlets-jboss-as7.zip