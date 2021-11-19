# Stringer with bitmask support

This is a fork and stand-alone package (so no need to use a different x/tools
altogether) of the `stringer` command from golang.org/x/tools

## Usage

```bash
$ go install github.com/adamhassel/stringer
```

```golang
// go:generate stringer -type=MyType -bitmask

type MyType uint8

const (
	FlagOne MyType = 1 << iota
	FlagTwo
	FlagThree
)
```

```sh
$ go generate
```
