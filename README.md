# ISAAC64 Go Module

[ISAAC64][isaac] is a fast cryptographic 64-bit random number generator.
The generator structure implements `math/rand.Source64`, but it can also
be used directly without an interface.

    $ go get github.com/stellarentropy/isaac64

Since it's a cryptographic random number generator, it's meaningful to
seed from `crypto/rand.Reader`:

```go
r := isaac64.New()
r.SeedFrom(rand.Reader)
```

Documentation: <https://godoc.org/github.com/stellarentropy/isaac64>

[isaac]: https://www.burtleburtle.net/bob/rand/isaacafa.html
