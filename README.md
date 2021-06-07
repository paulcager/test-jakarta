 1. Clone https://github.com/paulcager/test-jakarta.git
 2. mvn compile exec:java -Dexec.mainClass=org.paulcager.testj.Main
    * It will work.
 3. Import into intelliJ and run. 
    * It will fail `java.lang.ClassNotFoundException: javax.xml.soap.MessageFactory`

Note: Intellij accepts activation Jar, but rejects soap-api Jar. Soap-api seems to be a slightly newer
Jar version.

```
$ file -k *
jakarta.activation-api-1.2.2.jar: Zip archive data, at least v1.0 to extract Zip archive data, made by v?[0x314], extract using at least v1.0, last modified Sat Sep 15 14:46:07 2012, method=store
- data
jakarta.xml.soap-api-1.4.2.jar:   Java archive data (JAR) Zip archive data, made by v2.0, extract using at least v2.0, last modified Mon Aug 27 10:28:22 2012, uncompressed size 1119, method=deflate
- data
```

Both can be processed successfully by `jar tvf`.
