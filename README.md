# SystemVerilog Tester

The purpose of this project is to find all the supported and missing SystemVerilog features in various Verilog tools.

# Running

Initialize the submodules:
```
$ git submodule init
$ git submodule update
```

Build tools (optional, tools from `PATH` can be used):

```
make runners
```

And then just run:

```
$ make generate-tests -j$(nproc)
$ make -j$(nproc)
```

This should generate many log files for all the tools/tests combinations and an `out/report.html` file with a summary of the tested features and tools.

If you don't want to generate the report file, but are interested in just running all the tests, you can run:

```
make tests
```

## Supported tools

* [Yosys](http://www.clifford.at/yosys/)
* [Odin II](https://verilogtorouting.org/)
* [Verilator](https://www.veripool.org/wiki/verilator)
* [Icarus](http://iverilog.icarus.com/)
* [slang](https://github.com/MikePopoloski/slang)