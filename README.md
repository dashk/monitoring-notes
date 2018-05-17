# Random Notes on Tracing

## Nomenclature
Source: https://github.com/opentracing/specification/blob/master/specification.md
* *Trace*: A DAG of *Span*, with edges between spans defined as *references*
* *Reference*: Relationship between spans
* *Span*: Node in a trace with the following metadata
  * Basics: Operation name, start & end time
  * *Span Tags*: Zero or more key/value pairs
  * *Span Logs*: Zero or more key/value pairs with timestamps
    * Not supported in all tracing libraries
  * *References*: Zero or more casually-related *spans*
  * *Span Context*: Defined below
* *Span context*: Data required to refer to a distinct span across process boundary
  * *Baggage Items*: Key/value pairs that would be carried across boundary


## Related articles
* Nomenclature on tracing: https://github.com/opentracing/specification/blob/master/specification.md
* Brief intro to distributed tracing: https://medium.com/opentracing/distributed-tracing-in-10-minutes-51b378ee40f1
* Brief intro to cross-process tracing: http://opentracing.io/documentation/pages/api/cross-process-tracing.html
* LightStep's library for tracing: https://github.com/lightstep/lightstep-tracer-java
