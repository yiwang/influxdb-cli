InfluxDB-CLI
============

SQL CLI for InfluxDB

### Installation
```shell
npm install influxdb-cli
```

### Usage

```shell
InfluxDB SQL CLI
Usage: influxdb-cli

Options:
  -h, --hostname  Host [%s]      [default: "localhost"]
  --port          Port [%s]      [default: 8086]
  -u, --user      User [%s]      [default: "root"]
  -p, --password  Password [%s]  [default: "root"]
  -d, --database  Database [%s]  [default: "db"]
```

### Example

```shell
influxdb-cli -d redsmin -u user -p password
Influx> Connecting to http://localhost:8086/db/redsmin ...
Influx> ✔ ready
Influx> SELECT used_memory, used_memory_lua, used_memory_peak from info limit 10;
┌───────────────┬─────────────────┬─────────────┬─────────────────┬──────────────────┐
│ time          │ sequence_number │ used_memory │ used_memory_lua │ used_memory_peak │
├───────────────┼─────────────────┼─────────────┼─────────────────┼──────────────────┤
│ 1383952323268 │ 1300            │ 1889826     │ 31744           │ 1889826          │
│ 1383952323258 │ 1299            │ 1889826     │ 31744           │ 1889826          │
│ 1383952317262 │ 1298            │ 1889826     │ 31744           │ 1889826          │
│ 1383952317254 │ 1297            │ 1889826     │ 31744           │ 1889826          │
│ 1383952311270 │ 1296            │ 1963522     │ 31744           │ 1963522          │
│ 1383952311261 │ 1295            │ 1963522     │ 31744           │ 1963522          │
│ 1383952305260 │ 1294            │ 1926674     │ 31744           │ 1926674          │
│ 1383952305253 │ 1293            │ 1926674     │ 31744           │ 1926674          │
│ 1383952299261 │ 1292            │ 1889826     │ 31744           │ 1889826          │
│ 1383952299257 │ 1291            │ 1889826     │ 31744           │ 1889826          │
└───────────────┴─────────────────┴─────────────┴─────────────────┴──────────────────┘
Influx>
```