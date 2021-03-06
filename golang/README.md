
# graphql-go

## Simple http server

see [main.go](./graphql-go/http/main.go)

```
$ wrk -t12 -c400 -d30s --timeout 10s "http://localhost:8080/graphql?query={hello}"
Running 30s test @ http://localhost:8080/graphql?query={hello}
  12 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    70.75ms  102.05ms   1.15s    88.30%
    Req/Sec   842.60    246.89     2.42k    71.58%
  302338 requests in 30.07s, 41.52MB read
  Socket errors: connect 0, read 413, write 8, timeout 0
Requests/sec:  10053.90
Transfer/sec:      1.38MB
```

## Simple http server + [json-iterator](https://github.com/json-iterator/go)

see [main.go](./graphql-go/http+jsoniter/main.go)

```
$ wrk -t12 -c400 -d30s --timeout 10s "http://localhost:8080/graphql?query={hello}"
Running 30s test @ http://localhost:8080/graphql?query={hello}
  12 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    75.55ms  109.77ms   1.70s    87.66%
    Req/Sec     0.88k   249.28     2.17k    72.19%
  316608 requests in 30.09s, 43.48MB read
  Socket errors: connect 0, read 236, write 9, timeout 0
Requests/sec:  10522.81
Transfer/sec:      1.45MB
```

## gin framework

see [main.go](./graphql-go/gin/main.go)

```
$ wrk -t12 -c400 -d30s --timeout 10s "http://localhost:8080/graphql?query={hello}"
Running 30s test @ http://localhost:8080/graphql?query={hello}
  12 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    79.09ms  114.49ms   1.27s    87.47%
    Req/Sec     0.86k   234.53     2.24k    72.36%
  310036 requests in 30.09s, 47.01MB read
Requests/sec:  10304.10
Transfer/sec:      1.56MB
```

## [httprouter](https://github.com/julienschmidt/httprouter) framework

see [main.go](./graphql-go/httprouter/main.go)

```
$ wrk -t12 -c400 -d30s --timeout 10s "http://localhost:8080/graphql?query={hello}"
Running 30s test @ http://localhost:8080/graphql?query={hello}
  12 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    81.91ms  115.34ms   1.24s    87.57%
    Req/Sec   778.14    266.32     2.33k    72.14%
  278963 requests in 30.10s, 38.31MB read
Requests/sec:   9267.52
Transfer/sec:      1.27MB
```

## [echo](https://github.com/labstack/echo) framework

see [main.go](./graphql-go/echo/main.go)

```
$ wrk -t12 -c400 -d30s --timeout 10s "http://localhost:8080/graphql?query={hello}"
Running 30s test @ http://localhost:8080/graphql?query={hello}
  12 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    75.90ms  109.05ms   1.61s    88.04%
    Req/Sec   842.14    232.97     2.11k    72.22%
  302158 requests in 30.10s, 45.82MB read
  Socket errors: connect 0, read 9, write 0, timeout 0
Requests/sec:  10038.20
Transfer/sec:      1.52MB
```
