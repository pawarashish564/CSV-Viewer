<h1 align="center"> CSV-Viewer </h1>
<!-- </h1> -->
<p align="center">
<img src='https://img.shields.io/badge/made%20with%20%E2%9D%A4%EF%B8%8F%20-java%20-orange'> </a>
<img src="https://badgen.net/badge/Open%20Source%20%3F/Yes%21/blue?icon=github">
<img src="https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat">
<img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square">
<a href="https://gitmoji.carloscuesta.me">
  <img src="https://img.shields.io/badge/gitmoji-%20😜%20😍-FFDD67.svg?style=flat-square" alt="Gitmoji">
</a>
</p>
<!-- <p align="center"><h1>CSVViewer</h1></p> -->

CSVViewer is command line csv viewer in Pure Java.


# Install

```sh
git clone https://github.com/pawarashish564/CSV-Viewer.git
javac CSVViewer.java
csv-viewer.bat 
```
### From File

using `p` or `path` option

```sh
csv-viewer.bat -p _example/example.csv
```

## Display Options

### Default

```sh
 $ csv-viewer.bat -p demo.csv
+=====================+=====+=====+=====+
| Str                 | f1  | f2  | int |
|=====================|=====|=====|=====|
| Witcher             | 7.6 | 7.4 | 7   |
| TBC Hours Mystery   | 4.1 | 4.1 | 3   |
| TBC Hours Mystery-2 | 4.1 | 3.9 | 3   |
| 20/20               | 4.1 | 3.7 | 3   |
| Nightline           | 2.7 | 2.6 | 2   |
| Dateline Friday     | 4.1 | 4.1 | 3   |
| Dateline Sunday     | 3.5 | 3.2 | 3   |
| Life On the Train   | 1.2 | 1.5 | 3   |
| Big Bang Theory     | 9.2 | 9.5 | 9   |
| Demo Cycle          | 1.8 | 5.6 | 1   |
| Colors              | 6.7 | 8.9 | 10  |
| Tech Study          | 8.9 | 8.9 | 8   |
+=====================+=====+=====+=====+
```
### Limit Option

set display rows num.

```sh
 $ csv-viewer.bat -p _example/example.csv -l 2
+===================+=====+=====+=====+
| Str               | f1  | f2  | int |
|===================|=====|=====|=====|
| Witcher           | 7.6 | 7.4 | 7   |
| TBC Hours Mystery | 4.1 | 4.1 | 3   |
+===================+=====+=====+=====+
```

### Filter Option

set display condition.

```sh
 $ csv-viewer.bat -p Demo.csv -f "f1 > 3.5"
 +=====================+=====+=====+=====+
| Str                 | f1  | f2  | int |
|=====================|=====|=====|=====|
| Witcher             | 7.6 | 7.4 | 7   |
| TBC Hours Mystery   | 4.1 | 4.1 | 3   |
| TBC Hours Mystery-2 | 4.1 | 3.9 | 3   |
| 20/20               | 4.1 | 3.7 | 3   |
| Dateline Friday     | 4.1 | 4.1 | 3   |
| Big Bang Theory     | 9.2 | 9.5 | 9   |
| Colors              | 6.7 | 8.9 | 10  |
| Tech Study          | 8.9 | 8.9 | 8   |
+=====================+=====+=====+=====+
```

```sh
 $ csv-viewer.bat -p Demo.csv -f "f1 < 3.5"
+===================+=====+=====+=====+
| Str               | f1  | f2  | int |
|===================|=====|=====|=====|
| Nightline         | 2.7 | 2.6 | 2   |
| Life On the Train | 1.2 | 1.5 | 3   |
| Demo Cycle        | 1.8 | 5.6 | 1   |
+===================+=====+=====+=====+
```
<!-- 
### Multiple Filter Option

#### And

#### Or -->

### Sorting Options

```sh
 $ csv-viewer.bat -p Demo.csv -s "Str"
+=====================+=====+=====+=====+
| Str                 | f1  | f2  | int |
|=====================|=====|=====|=====|
| 20/20               | 4.1 | 3.7 | 3   |
| Big Bang Theory     | 9.2 | 9.5 | 9   |
| Colors              | 6.7 | 8.9 | 10  |
| Dateline Friday     | 4.1 | 4.1 | 3   |
| Dateline Sunday     | 3.5 | 3.2 | 3   |
| Demo Cycle          | 1.8 | 5.6 | 1   |
| Life On the Train   | 1.2 | 1.5 | 3   |
| Nightline           | 2.7 | 2.6 | 2   |
| TBC Hours Mystery   | 4.1 | 4.1 | 3   |
| TBC Hours Mystery-2 | 4.1 | 3.9 | 3   |
| Tech Study          | 8.9 | 8.9 | 8   |
| Witcher             | 7.6 | 7.4 | 7   |
+=====================+=====+=====+=====+
```

```sh
 $ csv-viewer.bat -p Demo.csv -s "Str DESC"
+=====================+=====+=====+=====+
| Str                 | f1  | f2  | int |
|=====================|=====|=====|=====|
| Witcher             | 7.6 | 7.4 | 7   |
| Tech Study          | 8.9 | 8.9 | 8   |
| TBC Hours Mystery-2 | 4.1 | 3.9 | 3   |
| TBC Hours Mystery   | 4.1 | 4.1 | 3   |
| Nightline           | 2.7 | 2.6 | 2   |
| Life On the Train   | 1.2 | 1.5 | 3   |
| Demo Cycle          | 1.8 | 5.6 | 1   |
| Dateline Sunday     | 3.5 | 3.2 | 3   |
| Dateline Friday     | 4.1 | 4.1 | 3   |
| Colors              | 6.7 | 8.9 | 10  |
| Big Bang Theory     | 9.2 | 9.5 | 9   |
| 20/20               | 4.1 | 3.7 | 3   |
+=====================+=====+=====+=====+
```
# Usage

```sh
 $ csv-viewer -h
Usage of csviewer:
  -f value
        filter
  -l int
        set max display rows num
  -p string
        set csv file path
  -s string
        sort by set value
        ex) col [DESC]?
```

# TODO

- [x] Set multi filters 
- [x] Column Selection similar to that of SQL