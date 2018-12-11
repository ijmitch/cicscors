Disclaimer: this is a public, informal discussion of CORS applied to CICS TS between interested parties. It is not endorsed by IBM.

# CORS requirements

CICS HTTP support is currently unhelpful if the web client (browser or REST client) sends the requests required to implement the [CORS protocol](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS).

In particular, CICS TS treats any OPTIONS request as an invalid request and returns an error to the client.

There is an [existing RFE asking for OPTIONS support (75575)](http://www.ibm.com/developerworks/rfe/execute?use_case=viewRfe&CR_ID=75575).

CORS always needs to be configured in a server responding to HTTP requests - for example, WebSphere Liberty requires [entries in its server.xml](https://www.ibm.com/support/knowledgecenter/SS7K4U_liberty/com.ibm.websphere.wlp.zseries.doc/ae/twlp_webcontainer_cors_config.html).

How could CICS begin to react more helpfully to OPTIONS requests?
