# rtc2018
These are files for Romanian Testing Conference 2018 Perofmance testing workshop &amp; training

## Links

### Test environment

(Note! This will be removed after the session)

 * Wordpress: http://rtc2018.absurdicum.net/
 * JSON example: http://rtc2018.absurdicum.net/example.json

### Important documents

 * JMeter user manual: https://jmeter.apache.org/usermanual/index.html
 * Groovy documentation: http://groovy-lang.org/documentation.html


### Cheat sheets:

 * XPath cheat sheet: https://devhints.io/xpath
 * CSS Seletor cheat sheet: https://gist.github.com/smutnyleszek/809a69dd05e1d5f12d01
 * JSONPath expression: http://goessner.net/articles/JsonPath/

### Tools

 * Zed Attack Proxy: https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project
 * Man in the middle proxy: https://mitmproxy.org/

## Running JMeter

Following properties are used by the wordpress-performance-tests.jmx:
 * threads
 * rampup
 * duration
 * maxsleep
 * minsleep
 * host

These are defining how the script is executed.

The test set is created with the following command:

```shell
jmeter -n -t wordpress-performance-tests.jmx -p better-system.properties \\
         -l results-$(date +"%Y-%m-%d-%H-%M") \\
         -j log-$(date +"%Y-%m-%d-%H-%M") \\
         -Jthreads=100 \\
         -Jrampup=3600 \\
         -Jduration=5400 \\
         -Jmaxsleep=5000 \\
         -Jminsleep=1000
```
