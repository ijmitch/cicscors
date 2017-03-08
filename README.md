Disclaimer: this is a public, informal discussion of CORS applied to CICS TS between interested parties. It is not endorsed by IBM.

# CORS requirements

CICS HTTP support is currently unhelpful if the web client (browser or REST client) sends the requests required to implement the [CORS protocol](https://spring.io/understanding/CORS).

In particular, CICS TS treats any OPTIONS request as an invalid request and returns an error to the client.

CORS always needs to be configured in a server responding to HTTP requests - for example, WebSphere Liberty requires [entries in it's server.xml](https://www.ibm.com/support/knowledgecenter/SS7K4U_liberty/com.ibm.websphere.wlp.zseries.doc/ae/twlp_webcontainer_cors_config.html).

How could CICS begin to react more helpfully to OPTIONS requests?
