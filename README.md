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
BenchmarkEcho_Param                     18558699                65.8 ns/op             0 B/op          0 allocs/op
BenchmarkGin_Param                      21309153                55.1 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_Param               27352346                44.5 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_Param                 25255612                46.5 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_Param5                     7278160               165 ns/op               0 B/op          0 allocs/op
BenchmarkGin_Param5                     12259808                97.9 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_Param5              14699972                82.8 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_Param5                13901722                85.0 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_Param20                    2491510               477 ns/op               0 B/op          0 allocs/op
BenchmarkGin_Param20                     4968230               238 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_Param20              5516090               218 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_Param20                5260452               224 ns/op               0 B/op          0 allocs/op
BenchmarkEcho_ParamWrite                 7366664               163 ns/op               8 B/op          1 allocs/op
BenchmarkGin_ParamWrite                 10823007               110 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_ParamWrite          15739791                77.9 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_ParamWrite            14193450                83.4 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_GithubStatic              13455735                90.3 ns/op             0 B/op          0 allocs/op
BenchmarkGin_GithubStatic               15436561                73.9 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_GithubStatic        30678020                36.7 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_GithubStatic          17474025                65.3 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_GithubParam                6900595               169 ns/op               0 B/op          0 allocs/op
BenchmarkGin_GithubParam                10155667               114 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_GithubParam         10941675               104 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_GithubParam           10810258               107 ns/op               0 B/op          0 allocs/op
BenchmarkEcho_GithubAll                    34119             35171 ns/op               0 B/op          0 allocs/op
BenchmarkGin_GithubAll                     47886             24841 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_GithubAll              62156             19233 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_GithubAll                58622             20113 ns/op               0 B/op          0 allocs/op
BenchmarkEcho_GPlusStatic               18097941                62.7 ns/op             0 B/op          0 allocs/op
BenchmarkGin_GPlusStatic                19550718                56.1 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_GPlusStatic         50540704                23.8 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_GPlusStatic           22765383                46.6 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_GPlusParam                12613610                93.5 ns/op             0 B/op          0 allocs/op
BenchmarkGin_GPlusParam                 14937699                77.1 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_GPlusParam          18578491                62.4 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_GPlusParam            18347317                63.6 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_GPlus2Params               8526776               140 ns/op               0 B/op          0 allocs/op
BenchmarkGin_GPlus2Params               12315268                94.4 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_GPlus2Params        14119084                82.7 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_GPlus2Params          14512272                81.1 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_GPlusAll                    741766              1565 ns/op               0 B/op          0 allocs/op
BenchmarkGin_GPlusAll                    1000000              1182 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_GPlusAll             1324416               891 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_GPlusAll               1282832               927 ns/op               0 B/op          0 allocs/op
BenchmarkEcho_ParseStatic               16936779                70.6 ns/op             0 B/op          0 allocs/op
BenchmarkGin_ParseStatic                19675899                64.0 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_ParseStatic         46651410                24.7 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_ParseStatic           24191812                48.8 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_ParseParam                13917127                83.2 ns/op             0 B/op          0 allocs/op
BenchmarkGin_ParseParam                 17189340                65.8 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_ParseParam          20266167                54.0 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_ParseParam            19645971                65.4 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_Parse2Params               9613044               112 ns/op               0 B/op          0 allocs/op
BenchmarkGin_Parse2Params               16091012                74.8 ns/op             0 B/op          0 allocs/op
BenchmarkHttpRouter_Parse2Params        18267997                63.7 ns/op             0 B/op          0 allocs/op
BenchmarkCleverGo_Parse2Params          18200055                67.4 ns/op             0 B/op          0 allocs/op
BenchmarkEcho_ParseAll                    406428              2702 ns/op               0 B/op          0 allocs/op
BenchmarkGin_ParseAll                     566844              1854 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_ParseAll              891412              1334 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_ParseAll                702619              1582 ns/op               0 B/op          0 allocs/op
BenchmarkEcho_StaticAll                    54938             22273 ns/op               0 B/op          0 allocs/op
BenchmarkGin_StaticAll                     68902             17419 ns/op               0 B/op          0 allocs/op
BenchmarkHttpRouter_StaticAll             121804              9614 ns/op               0 B/op          0 allocs/op
BenchmarkCleverGo_StaticAll                80704             14777 ns/op               0 B/op          0 allocs/op
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
