# PoshOtel
An Open Telemetry Client for use in PowerShell scripts

This is very experimental. Lots of work-in-progress and missing tests / more robust methods before this is ready for prime time.

Currently, this will output syncronous events to an OTLP endpoint configured as below. I have only tested with this Honeycomb so far.

test/TestConsumer.ps1 has proof-of-concept examples while functionality is being built.

Here's a very basic trace in Honeycomb:
![image](https://user-images.githubusercontent.com/2453236/153727442-77d02af4-8d79-47b4-8488-b19af90dd1b1.png)


## Environment Variables

```powershell
    $env:OTEL_EXPORTER_OTLP_ENDPOINT = 'https://api.honeycomb.io:443'
    $env:OTEL_EXPORTER_OTLP_HEADERS = 'x-honeycomb-team=<<API_KEY>>,x-honeycomb-dataset=<<DATASET>>'
    $env:OTEL_EXPORTER_OTLP_TIMEOUT = '600000'
    $env:OTEL_EXPORTER_OTLP_PROTOCOL = 'grpc'
```

