# ezmq

FIXME: write description

## Usage

Requires a functional ZMQ/JZMQ installation. You'll need to have the
native interface working and `zmq.jar` in the `lib/` directory. On
Linux/OSX/Windows the easiest way to do this is via lein native-deps.

### Native Deps

Install ZMQ (tested using the 2.1.11 branch) and then modify your `project.clj`

```Clojure
(defproject ...
  ...
  :dependencies [[ezmq "0.0.1"] ...]
  :dev-dependencies [[native-deps "1.0.5"] ...]
  :native-dependencies [[org.clojars.starry/jzmq-native-deps "2.0.10"] ...]
  :native-path "/usr/local/lib")
```

then get the dependencies with `lein deps` followed by `lein native-deps`.

Native dependencies are not added to the dependency tree! All projects
which depend upon `ezmq` will need to set up ZMQ/JZMQ themselves or
replicate these `native-deps` instructions in the project specific
`project.clj`.

### Then—

```Clojure
(ns my.namespace
  (:use [ezmq.core :as mq]))
```

## License

Copyright (C) 2012 Joseph Abrahamson

Distributed under the Eclipse Public License, the same as Clojure.
