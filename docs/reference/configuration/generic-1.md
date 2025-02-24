# Generic

All sinks in Firehose requires the following variables to be set

## `KAFKA_RECORD_PARSER_MODE`

Decides whether to parse key or message \(as per your input proto\) from incoming data.

* Example value: `message`
* Type: `required`
* Default value`: message`

## `SINK_TYPE`

Defines the Firehose sink type.

* Example value: `log`
* Type: `required`

## `INPUT_SCHEMA_PROTO_CLASS`

Defines the fully qualified name of the input proto class.

* Example value: `com.tests.TestMessage`
* Type: `required`

## `INPUT_SCHEMA_PROTO_TO_COLUMN_MAPPING`

Defines the mapping of the Proto fields to header/query fields in JSON format.

* Example value: `{"1":"order_number","2":"event_timestamp","3":"driver_id"}`
* Type: `optional`

## `METRIC_STATSD_HOST`

URL of the StatsD host \(Telegraf service\)

* Example value: `localhost`
* Type: `optional`
* Default value`: localhost`

##  `METRIC_STATSD_PORT`

Port of the StatsD host \(Telegraf service\)

* Example value: `8125`
* Type: `optional`
* Default value`: 8125`

## `METRIC_STATSD_TAGS`

Global tags for StatsD metrics. Tags must be comma-separated.

* Example value: `team=data-engineering,app=firehose`
* Type: `optional`

## `FILTER_JEXL_DATA_SOURCE`

`key`/`message`/`none`depending on where to apply filter

* Example value: `key`
* Type: `optional`
* Default value`: none`

## `FILTER_JEXL_EXPRESSION`

JEXL filter expression

* Example value: `driverLocationLogKey.getVehicleType()=="BIKE"`
* Type: `optional`

## `FILTER_JEXL_SCHEMA_PROTO_CLASS`

The fully qualified name of the proto schema so that the key/message in Kafka could be parsed.

* Example value: `com.gojek.esb.driverlocation.DriverLocationLogKey`
* Type: `optional`

## `APPLICATION_THREAD_CLEANUP_DELAY`

Defines the time duration in milliseconds after which to cleanup the thread.

* Example value: `400`
* Type: `optional`
* Default value: `2000`

## `APPLICATION_THREAD_COUNT`

Number of parallel threads to run for Firehose.

* Example value: `2`
* Type: `optional`
* Default value: `1`

## `TRACE_JAEGAR_ENABLE`

Defines whether to enable Jaegar tracing or not

* Example value: `true`
* Type: `optional`
* Default value: `false`

