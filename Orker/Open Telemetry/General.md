Open Telemetry

When to use a collector
For most language specific instrumentation libraries you have exporters for popular backends and OTLP. You might wonder,

under what circumstances does one use a collector to send data, as opposed to having each service send directly to the backend?

For trying out and getting started with OpenTelemetry, sending your data directly to a backend is a great way to get value quickly. Also, in a development or small-scale environment you can get decent results without a collector.

However, in general we recommend using a collector alongside your service, since it allows your service to offload data quickly and the collector can take care of additional handling like retries, batching, encryption or even sensitive data filtering.

It is also easier to setup a collector than you might think: the default OTLP exporters in each language assume a local collector endpoint, so if you launch a collector it will automatically start receiving telemetry.

--

Prometheus : Metrics
Jaeger : Traces
