# PrimalEx

NIF Elixir bindings for the [Primal](https://github.com/huonw/primal) Rust library.

It utilizes the [Rustler](https://github.com/hansihe/rustler) library to handle the NIF interop, which may or may not be production-ready. Be aware of the caveats outlined in [this blog post.](http://hansihe.com/2017/02/05/rustler-safe-erlang-elixir-nifs-in-rust.html)

## Installation
The package can be installed
by adding `prime_ex` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [{:primal_ex, "~> 0.1.0"}]
end
```

## Usage examples

```elixir

# Get a list of primes less than 40
PrimalEx.primes(40)
{:ok, [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37]}

# Get a list of the first 10 primes
PrimalEx.n_primes(10)
{:ok, [2, 3, 5, 7, 11, 13, 17, 19, 23, 29]}

```

