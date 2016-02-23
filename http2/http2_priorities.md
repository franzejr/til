# HTTP Priorities

The purpose of prioritization is to allow an endpoint to express how it would prefer its peer to allocate resources when managing concurrent streams. 
Most importantly, priority can be used to select streams for transmitting frames when there is limited capacity for sending.

Streams can be prioritized by marking them as dependent on the completion of other streams (Section 5.3.1). 
Each dependency is assigned a relative weight, a number that is used to determine the relative proportion of available resources that are assigned to streams dependent on the same stream.

Priority can be by content-type. For example, download firstly javascript and after html and css for example.

Example using nghttpd for a HTTP/2 server.

Source: https://http2.github.io/http2-spec/#rfc.section.5.3
