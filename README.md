Shibboleth Identity Provider in Docker
--------------------------------------

!POC!

Install Shibboleth IdP in tomcat in a Centos 6, with a JAAS login example

Build it
docker build -t demo/ipd .

Run it with
docker run -dt -v /Users/jonas/tmp:/opt/shibboleth-idp/metadata/ -p 8444:8443 demo/ipd 

Copy the generated IDP metadata to your SP
docker cp <containerid>:/opt/shibboleth-idp/metadata/idp-metadata.xml .
