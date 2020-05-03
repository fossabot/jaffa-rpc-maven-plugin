## How to use transport-maven-plugin

This plugin is a part of transport library project and supposed to 
create transport client interfaces.  
To turn off source generation - disable corresponding maven profile (like "generate-transport-api" in example below):

```
<properties>
    <root-path>src/main/java/</root-path>
    <root-package>com.transport</root-package>
</properties>
<profiles>
        <profile>
            <id>generate-transport-api</id>
            <build>
                <plugins>
                    <plugin>
                        <groupId>com.edwardhyde</groupId>
                        <artifactId>transport-maven-plugin</artifactId>
                        <version>1.0-SNAPSHOT</version>
                        <configuration>
                            <root-path>${root-path}</root-path>
                            <root-package>${root-package}</root-package>
                        </configuration>
                        <executions>
                            <execution>
                                <goals>
                                    <goal>generate-transport-api</goal>
                                </goals>
                            </execution>
                        </executions>
                    </plugin>
                </plugins>
            </build>
        </profile>
    </profiles>
```
