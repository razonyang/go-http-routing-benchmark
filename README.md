Go HTTP Router Benchmark
========================

This benchmark suite aims to compare the performance of HTTP request routers for [Go](https://golang.org) by implementing the routing structure of some real world APIs.
Some of the APIs are slightly adapted, since they can not be implemented 1:1 in some of the routers.

Of course the tested routers can be used for any kind of HTTP request → handler function routing, not only (REST) APIs.

 * [CleverGo](https://github.com/clevergo/clevergo)
 * [Echo](https://github.com/labstack/echo)
 * [Gin](https://github.com/gin-gonic/gin)
 * [HttpRouter](https://github.com/julienschmidt/httprouter)

 ![Benchmark](https://clevergo.tech/img/benchmark.png)

## Results

```text
BenchmarkEcho_Param                     17208848                67.2 ns/op             0 B/op          0 allocs/op
BenchmarkGin_Param                      19626481                62.1 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_Param               26328606                45.5 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_Param                 22108220                50.5 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_Param5                     6766945               178 ns/op               0 B/op          0 allocs/op
BenchmarkGin_Param5                     11362148               106 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_Param5              14033802                86.2 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_Param5                12487436                97.1 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_Param20                    2172370               547 ns/op               0 B/op          0 allocs/op
BenchmarkGin_Param20                     4237574               282 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_Param20              5126389               238 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_Param20                4640288               254 ns/op               0 B/op          0 allocs/op
BenchmarkEcho_ParamWrite                 7421761               165 ns/op               8 B/op          1 allocs/op
BenchmarkGin_ParamWrite                 10331936               115 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_ParamWrite          15103327                78.1 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_ParamWrite            13360153                87.8 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_GithubStatic              12522909                91.7 ns/op             0 B/op          0 allocs/op
BenchmarkGin_GithubStatic               15946930                72.0 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_GithubStatic        28753052                39.4 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_GithubStatic          18188330                62.8 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_GithubParam                6755791               174 ns/op               0 B/op          0 allocs/op
BenchmarkGin_GithubParam                 9510400               127 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_GithubParam         11378728               104 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_GithubParam           10426410               114 ns/op               0 B/op          0 allocs/op
BenchmarkEcho_GithubAll                    33564             36874 ns/op               0 B/op          0 allocs/op
BenchmarkGin_GithubAll                     45387             25552 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_GithubAll              66373             19216 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_GithubAll                57278             20800 ns/op               0 B/op          0 allocs/op
BenchmarkEcho_GPlusStatic               18656060                63.5 ns/op             0 B/op          0 allocs/op
BenchmarkGin_GPlusStatic                19757514                60.3 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_GPlusStatic         49875481                23.9 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_GPlusStatic           24655155                45.9 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_GPlusParam                12652534                92.9 ns/op             0 B/op          0 allocs/op
BenchmarkGin_GPlusParam                 14641348                79.8 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_GPlusParam          18865038                62.4 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_GPlusParam            17895858                65.4 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_GPlus2Params               8499931               140 ns/op               0 B/op          0 allocs/op
BenchmarkGin_GPlus2Params               11289526               105 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_GPlus2Params        14275208                83.7 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_GPlus2Params          13555339                84.9 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_GPlusAll                    757988              1518 ns/op               0 B/op          0 allocs/op
BenchmarkGin_GPlusAll                    1000000              1101 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_GPlusAll             1498773               793 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_GPlusAll               1333015               884 ns/op               0 B/op          0 allocs/op
BenchmarkEcho_ParseStatic               18583479                68.8 ns/op             0 B/op          0 allocs/op
BenchmarkGin_ParseStatic                18936175                62.0 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_ParseStatic         45943996                25.3 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_ParseStatic           23756925                49.2 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_ParseParam                14461281                80.7 ns/op             0 B/op          0 allocs/op
BenchmarkGin_ParseParam                 17845074                66.1 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_ParseParam          23658338                49.5 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_ParseParam            21278804                56.2 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_Parse2Params              10346294               115 ns/op               0 B/op          0 allocs/op
BenchmarkGin_Parse2Params               13889582                85.4 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_Parse2Params        18141990                61.7 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_Parse2Params          17130621                68.3 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_ParseAll                    429348              2644 ns/op               0 B/op          0 allocs/op
BenchmarkGin_ParseAll                     577339              1965 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_ParseAll              843637              1331 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_ParseAll                709344              1613 ns/op               0 B/op          0 allocs/op
BenchmarkEcho_StaticAll                    49203             23958 ns/op               0 B/op          0 allocs/op
BenchmarkGin_StaticAll                     61629             19234 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_StaticAll             108595             10791 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_StaticAll                73195             16265 ns/op               0 B/op          0 allocs/op
```

## Usage

If you'd like to run these benchmarks locally, you'll need to install the package first:

```bash
go get github.com/razonyang/go-http-routing-benchmark
```
This may take a while due to the large number of dependencies that need to be downloaded. Once that command has finished you can run the full set of benchmarks like this:

```bash
cd $GOPATH/src/github.com/razonyang/go-http-routing-benchmark
go test -bench=.
```

> **Note:** If you run the tests and it SIGQUIT's make the go test timeout longer (#44)
>
```
go test -timeout=2h -bench=.
```


You can bench specific frameworks only by using a regular expression as the value of the `bench` parameter:
```bash
go test -bench="CleverGo|Gin|Echo"
```
