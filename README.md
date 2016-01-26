# test2junit

[![Clojars Project](http://clojars.org/test2junit/latest-version.svg)](http://clojars.org/test2junit)

A `leiningen plug-in` to output test results to JUnit XML format.
  
These files can be used, e.g., with junitreport for creating reports in HTML format.
  
You can tweak some setting via your `project.clj` file:

```clojure
  ; specify your output directory
  :test2junit-output-dir "test-results"

  ; to run ant automatically
  :test2junit-run-ant true
```

Example junit report output based on the output as generated by this plug-in is available at:
http://ruedigergad.github.com/clj-assorted-utils/test-results/html/

To use this plug-in simply add `[test2junit "1.2.1"]` either to your `~/.lein/profile.clj` or as 
development dependency to an individual project. 
_test2junit_ requires _Leiningen 2.x_.

## Usage Example

Below is an example for globally adding test2junit via the ~/.lein/profiles.clj    file:

    {:user {:plugins [[test2junit "1.2.1"]]}}

Or you can just add it to your development profile like so:

    :profiles {:dev {:plugins [[test2junit "1.2.1"]]}}

An example for the project specific setting can be found in:
https://github.com/ruedigergad/clj-assorted-utils/blob/master/project.clj

This will enable you to use the plugin from your terminal:
    
    $ lein test2junit

## License

Copyright © 2013 Ruediger Gad, et al. (See src/test2junit/junit.clj).

Distributed under the Eclipse Public License, the same as Clojure.
