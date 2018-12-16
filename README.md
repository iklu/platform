Err (clean package dockerfile:build)

WARNING: HK2 service reification failed for [org.glassfish.jersey.message.internal.DataSourceProvider] when building with JDK 11


You can work around these warnings by adding a dependency to your plugin definition:

            <plugin>
                <groupId>com.spotify</groupId>
                <artifactId>dockerfile-maven-plugin</artifactId>
[...]
                <dependencies>
                    <dependency>
                        <groupId>javax.activation</groupId>
                        <artifactId>activation</artifactId>
                        <version>1.1.1</version>
                    </dependency>
                </dependencies>
            </plugin>


