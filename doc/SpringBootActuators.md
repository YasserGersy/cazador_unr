Spring Boot includes a number of built-in endpoints (or endpoints for Spring Boot 1.x) and lets developers add their own. For example, the health endpoint provides basic application health information.
Each individual endpoint can be enabled or disabled and exposed over `HTTP` or `JMX`. An endpoint is considered to be available when it is both enabled and exposed. The built-in endpoints will only be auto-configured when they are available. Most applications choose exposure via HTTP, where the ID of the endpoint along with a prefix of `/actuator` is mapped to a URL. For example, by default, the health endpoint is mapped to `/actuator/health`.

Full-list:`https://github.com/YasserGersy/Enums/blob/master/Knowledge/spring.boot.acuts.txt`

Interesting Endpoints:

```
/actuator/autoconfig
/actuator/beans/
/actuator/configprops/
/actuator/dump
/actuator/heapdump
/actuator/env/
/actuator/health
/actuator/info
/actuator/loggers/
/actuator/mappings/
/actuator/metrics/
/actuator/shutdown
/actuator/trace
```

Other End-points [from docs.spring.io](https://docs.spring.io/spring-boot/docs/current/reference/html/actuator.html#actuator.endpoints) : 

```
/logfile
/prometheus
/heapdump
/threaddump
/startup
/shutdown
/sessions
/scheduledtasks
/quartz
/mappings
/metrics
/liquibase
/loggers
/integrationgraph
/info
/httpexchanges
/health
/flyway
/env
/configprops
/conditions
/caches
/beans
/auditevents
/actuator
/autoconfig
/docs
/dump
/httptrace
/intergrationgraph
/jolokia
/refresh
/trace
/actuator/auditevents
/actuator/beans
/actuator/health
/actuator/conditions
/actuator/configprops
/actuator/env
/actuator/info
/actuator/loggers
/actuator/heapdump
/actuator/threaddump
/actuator/metrics
/actuator/scheduledtasks
/actuator/httptrace
/actuator/mappings
/actuator/jolokia
/actuator/hystrix.stream
```

Shodan
```
org:YOUR_TARGET http.favicon.hash:116323821
```

REF:

```
- https://0xn3va.gitbook.io/cheat-sheets/framework/spring/spring-boot-actuators

```
