# clj-blend

Clojure library for interacting with Galaxy, CloudMan, and BioCloudCentral. This
builds on [blend4j][0] with lots of help from [blend][1]. Provides high level
functionality on top of blend4j, with a focus on smooth interaction with Galaxy.

[0]: https://github.com/jmchilton/blend4j
[1]: https://github.com/afgane/blend

## Usage

Requires Java 1.6 or better and [Leiningen 2.x][u1].

    $ lein repl
    > (require '[blend.galaxy.core :as galaxy])
    > (def c (galaxy/get-client "https://main.g2.bx.psu.edu/" "your-api-key"))
    > (def ds (galaxy/get-datasets-by-type c :bed))
    > (galaxy/download-dataset c (first ds) "/where/to/put/your/file.bed")
    > (galaxy/upload-to-history c "http://www.yoursite.com/data" :hg19 :vcf)
    

[u1]: https://github.com/technomancy/leiningen

## License

The code is freely available under the [MIT license][l1].

[l1]: http://www.opensource.org/licenses/mit-license.html
