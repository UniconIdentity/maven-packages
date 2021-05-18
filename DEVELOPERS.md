Example command to upload package:
```
mvn deploy:deploy-file -Dfile=duo-java-1.1.jar -Durl=https://maven.pkg.github.com/UniconIdentity/maven-packages -Dpacking=jar -DgroupId=net.unicon.iam -DartifactId=duo-java -Dversion=1.1 -DrepositoryId=github
```

You will need a settings.xml with:

```
<?xml version="1.0" encoding="UTF-8"?>
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 http://maven.apache.org/xsd/settings-1.0.0.xsd">
    
    <servers>
    <server>
        <id>github</id>
        <username>USERNAME_HERE</username>
        <password>YOUR_PERSONAL_ACCESS_TOKEN_CREATED_IN_YOUR_GITHUB_ACCOUNT_WITH_PACKAGE_WRITE_HERE</password>
    </server>
    </servers>
</settings>
```
