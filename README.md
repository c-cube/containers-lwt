# Containers-lwt

Small suite of utilities for Lwt. BSD license.

**not released yet**

## Build

Depends on [lwt](https://github.com/ocsigen/lwt/) and
[containers](https://github.com/c-cube/ocaml-containers).

Use opam, for instance:

    opam pin add -k git containers-lwt https://github.com/c-cube/containers-lwt.git

and

    opam install containers-lwt

## Use

The library contains a pack module `Containers_lwt`, with the following modules:

- `Lwt_klist`: a lazy list of values compatible with `Lwt`. Resembles `Lwt_stream`
   but with memoization, as a pure value.
- `Lwt_pipe`: a (bounded or unbounded) pipe between consumer(s) and producer(s)
   with a focus on safety and efficiency. The point is that pushing
   and poping can block, thus limiting the resource consumption
   if producers are faster than consumers.

Less stable/usable:

- `Lwt_actor`: experimental simplistic actor library on top of `Lwt`
- `Lwt_automaton`: experimental automatons on top of `Lwt`
