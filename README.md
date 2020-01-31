
# Run command
Here is the mvn command that emulates the one failing in the pipeline.
I have deliberately called the property myrevision so it is different from the one used in hippo
``` 
mvn verify -Dmyrevision=v3.0.427 -D skipTests=true
```


### Errors on this project
``` 
[ERROR] [ERROR] Some problems were encountered while processing the POMs:
[FATAL] Non-resolvable parent POM for org.example:myproject-cms-dependencies:[unknown-version]: Could not find artifact org.example:myproject:pom:0.1.0-SNAPSHOT and 'parent.relativePath' points at wrong local POM @ line 5, column 11
[FATAL] Non-resolvable parent POM for org.example:myproject-repository-data:[unknown-version]: Could not find artifact org.example:myproject:pom:0.1.0-SNAPSHOT and 'parent.relativePath' points at wrong local POM @ line 5, column 11
[FATAL] Non-resolvable parent POM for org.example:myproject-cms:[unknown-version]: Could not find artifact org.example:myproject:pom:0.1.0-SNAPSHOT and 'parent.relativePath' points at wrong local POM @ line 5, column 11
[FATAL] Non-resolvable parent POM for org.example:myproject-components:[unknown-version]: Could not find artifact org.example:myproject-site:pom:0.1.0-SNAPSHOT and 'parent.relativePath' points at wrong local POM @ line 5, column 11
[FATAL] Non-resolvable parent POM for org.example:myproject-webapp:[unknown-version]: Could not find artifact org.example:myproject-site:pom:0.1.0-SNAPSHOT and 'parent.relativePath' points at wrong local POM @ line 5, column 11
[FATAL] Non-resolvable parent POM for org.example:myproject-essentials:[unknown-version]: Could not find artifact org.example:myproject:pom:0.1.0-SNAPSHOT and 'parent.relativePath' points at wrong local POM @ line 5, column 11
 @ 

```


### Errors from hippo pipeline
```
[ERROR] [ERROR] Some problems were encountered while processing the POMs:
[FATAL] Non-resolvable parent POM for uk.nhs.digital:website:${revision}: 
Could not transfer artifact com.onehippo.cms7:hippo-cms7-enterprise-release:pom:13.2.2 
from/to hippo-maven2-enterprise (https://maven.onehippo.com/maven2-enterprise): 


Not authorized and 'parent.relativePath' points at wrong local POM @ line 9, column 13

```