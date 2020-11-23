# slices and arrays

https://www.sohamkamani.com/blog/golang/arrays-vs-slices/

https://programming.guide/go/nil-slice-vs-empty-slice.html

https://medium.com/rungo/the-anatomy-of-slices-in-go-6450e3bb2b94

https://www.callicoder.com/golang-slices/

https://github.com/golang/go/wiki/SliceTricks

https://go101.org/article/memory-leaking.html

### sources
https://github.com/golang/go/blob/440f7d64048cd94cba669e16fe92137ce6b84073/src/runtime/slice.go

https://github.com/golang/go/blob/440f7d64048cd94cba669e16fe92137ce6b84073/src/runtime/slice_test.go


# maps

https://medium.com/rungo/the-anatomy-of-maps-in-go-79b82836838b

https://www.callicoder.com/golang-maps/
https://www.ardanlabs.com/blog/2013/12/macro-view-of-map-internals-in-go.html

### sources
https://github.com/golang/go/blob/master/src/runtime/map.go
https://github.com/golang/go/blob/440f7d64048cd94cba669e16fe92137ce6b84073/src/runtime/map_benchmark_test.go
https://github.com/golang/go/blob/440f7d64048cd94cba669e16fe92137ce6b84073/src/runtime/map_test.go

# channels 

https://github.com/quii/learn-go-with-tests/blob/master/concurrency.md

https://github.com/quii/learn-go-with-tests/tree/master/concurrency

https://docs.google.com/document/d/1-n2O-c3C6kz-4vNKJdtR9bjh-kXqJe7RydSOTBxvB3g/edit?usp=sharing

https://habr.com/ru/post/308070/

https://github.com/quii/learn-go-with-tests/tree/master/select

https://www.ardanlabs.com/blog/2017/10/the-behavior-of-channels.html


# package oriented design

https://www.ardanlabs.com/blog/2019/09/context-package-semantics-in-go.html

https://golang.org/pkg/context/

https://habr.com/ru/company/nixys/blog/461723/  


# scheduller

https://docs.google.com/presentation/d/1UCOEHw-0oSUiOA94aTX79Ki7VbsmPtlYlv1EfyI1ylE/edit#slide=id.p

https://www.ardanlabs.com/blog/2018/08/scheduling-in-go-part1.html

https://habr.com/ru/post/333654/

https://github.com/golang/go/blob/master/src/runtime/proc.go


# sync poll

https://habr.com/ru/post/277137/

https://dev-gang.ru/article/go-ponjat-dizain-syncpool-cpvecztx8e/

https://golang.org/src/sync/pool.go

https://medium.com/a-journey-with-go/go-understand-the-design-of-sync-pool-2dde3024e277

# pointers

https://github.com/quii/learn-go-with-tests/blob/master/pointers-and-errors.md

https://github.com/quii/learn-go-with-tests/tree/master/pointers

https://medium.com/@vCabbage/go-are-pointers-a-performance-optimization-a95840d3ef85

https://rtfm.co.ua/golang-ukazateli-podrobnyj-razbor/

https://habr.com/ru/post/339192/

https://medium.com/a-journey-with-go/go-should-i-use-a-pointer-instead-of-a-copy-of-my-struct-44b43b104963
https://www.ardanlabs.com/blog/2017/05/language-mechanics-on-stacks-and-pointers.html

https://www.ardanlabs.com/blog/2017/05/language-mechanics-on-stacks-and-pointers.html

 
# profiling

https://www.ardanlabs.com/blog/2017/06/language-mechanics-on-memory-profiling.html
https://golang.org/pkg/runtime/pprof/
https://golang.org/doc/diagnostics.html

https://habr.com/ru/company/badoo/blog/301990/

https://www.freecodecamp.org/news/how-i-investigated-memory-leaks-in-go-using-pprof-on-a-large-codebase-4bec4325e192/

# context

https://github.com/quii/learn-go-with-tests/blob/master/context.md
https://github.com/quii/learn-go-with-tests/tree/master/context

https://www.ardanlabs.com/blog/2019/09/context-package-semantics-in-go.html

https://golang.org/pkg/context/

https://habr.com/ru/company/nixys/blog/461723/

# gc
https://www.ardanlabs.com/blog/2018/12/garbage-collection-in-go-part1-semantics.html
https://blog.golang.org/ismmkeynote
https://www.facebook.com/watch/?v=871606259683390
https://habr.com/ru/post/265833/

https://github.com/golang/go/blob/50bd1c4d4eb4fac8ddeb5f063c099daccfb71b26/src/runtime/debug/garbage.go

https://github.com/golang/go/blob/7955ecebfc85851d43913f9358fa5f6a7bbb7c59/src/runtime/extern.go

https://github.com/golang/go/blob/05511a5c0ae238325c10b0e4e44c3f66f928e4cf/src/runtime/mgc.go

# escape analysis

https://www.ardanlabs.com/blog/2017/05/language-mechanics-on-escape-analysis.html

https://habr.com/ru/company/intel/blog/422447/