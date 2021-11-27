# demo - goldly


## Static Demo

A simple demo is on [Github Pages](https://pink-gorilla.github.io/demo-goldly/).

There are no server services running in the static demo. 
So the time pusher and the fortune cookies will not work.


## demo running goldly-docs

Goldly-docs brings everything precompiled. Saves lots of time.

First, clone this repo. Then run: `clojure -X:goldly-docs`
After starting, open web-browser on port 8080.

The snippets are primitive, but demonstrate certain features of goldly:
- bmi: complex ui interaction
- fortune cookies: demonstrates how to load data from clojure (could be a database)
- time: demonstrates to push data from clojure
- iss: international space stations current position


## demo with custom dynamic cljs build (watch mode)

You only need to build a custom cljs build:
- if you want to use ui-components that are not included in goldly-docs.
- if you want you want to compile your own clojurescript code.
  (this could be relevant if you need say core.async which is not available in 
  sci interpreted clojurescript)

For this demo, it is not neccesary to build cljs. But lets do it for fun anyhow.

The following commands will build a bundel, and recompile it in case a source file
changes. Shadow-cljs calls this "watch".

`clojure -X:goldly`

You can use *"watch"* which brings 10x developer tools.
Or you can use *"watch2"* which does not. 10x developer tools make the bundel bigger,
but could be helpful for debugging.

## demo - compile custom cljs and then run it. (for deployment)

This involves two steps:
- *compiling* a javascript bundel (output is in target/webly/public)
- *running* a web server and serving the page/bundel. 
  After you compiled the bundel you can run it multiple times.  

 `./scripts/compile_adv_run.sh`


