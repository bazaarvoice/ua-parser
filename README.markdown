**Caution**: This project is a fork of the User Agent String Parser, which is currently found on GitHub at
https://github.com/ua-parser. The Java implementation is located at https://github.com/ua-parser/uap-java.

## Why is there a fork?

Unfortunately, the upstream project does not appear to publish artifacts to Maven Central, and releases are quite infrequent. This fact necessitated the creation of a fork, as we needed the ability to publish an artifact within our Sonatype Nexus repository. In addition, the upstream version contains a security vulnerability that is mitigated within our fork.

## What is different?

* The project has been modified to use the BV Super POM.
* The linked version of Apache Commons has been upgraded to mitigate a security vulnerability.
* The project structure differs from that of the upstream project, which has moved to a different repository since the original fork appeared.
* This version has been patched to include the changes made between upstream 1.2.0 and 1.3.1, while still preserving the old directory structure.
* This version includes the newest (as of 1.3.1) regex patterns and tests, which include detection support for browsers like Microsoft Edge.

----

ua-parser
=========

`ua-parser` is a multi-language port of [BrowserScope][2]'s [user agent string parser][3].

The crux of the original parser--the data collected by [Steve Souders][4] over the years--has been extracted into a separate [YAML file][5] so as to be reusable _as is_ by implementations in other programming languages. `ua-parser` is just a small wrapper around this data, along with ongoing improvements to the definitions.

Note that `ua-parser` has now been split out into multiple, distinct repositories, one for the [core definitions][6] and one for each [language implementation][7]. Patches and issues should be raised at those repositories, rather than this one.


[1]: http://nodejs.org
[2]: http://www.browserscope.org
[3]: http://code.google.com/p/ua-parser/
[4]: http://stevesouders.com/
[5]: https://raw.github.com/tobie/ua-parser/master/regexes.yaml
[6]: https://github.com/ua-parser/uap-core
[7]: https://github.com/ua-parser
