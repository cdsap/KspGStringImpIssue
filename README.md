### Ksp issue with Android project using groovy.

#### Error
```
> Failed to query the value of task ':app:kspDebugKotlin' property 'pluginOptions'.
      > Failed to query the value of task ':app:kspDebugKotlin' property 'options'.
         > class org.codehaus.groovy.runtime.GStringImpl cannot be cast to class java.lang.String (org.codehaus.groovy.runtime.GStringImpl is in unnamed module of loader org.gradle.internal.classloader.VisitableURLClassLoader @4667ae56; java.lang.String is in module java.base of loader 'bootstrap')
```

#### Steps to reproduce it
1. Clone repo
2. Execute `./gradlew :app:assembleDebug`

More details on the stacktrace https://ge.solutions-team.gradle.com/s/tuqnaigqc5yyq/failure#1


### Notes
This issue is only reproducible when using build.gradle, with kts it works.
