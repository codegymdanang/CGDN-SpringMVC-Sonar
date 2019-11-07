# CodeGymDaNang-Spring Sonar
1. Cài đặt sonarlink kiểm tra chất lượng code trên intelligi
<img width="1015" alt="Screen Shot 2019-11-06 at 8 25 43 PM" src="https://user-images.githubusercontent.com/37821007/68302062-d2071380-00d3-11ea-866c-8c6a91d70cc3.png">

2. Check chất lượng code local bằng sonarlink
<img width="1197" alt="Screen Shot 2019-11-06 at 8 40 57 PM" src="https://user-images.githubusercontent.com/37821007/68303175-e6e4a680-00d5-11ea-87e6-981a9d9ab193.png">

3. POM plugin sonarlink server

```
<profiles>
		<profile>
			<id>sonar</id>
			<activation>
				<activeByDefault>true</activeByDefault>
			</activation>
			<properties>
				<!-- Optional URL to server. Default value is http://localhost:9000 -->
				<sonar.host.url>
				   http://codegymdanang.com:1051/
				</sonar.host.url>
			</properties>
		</profile>
	</profiles>

	<build>
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<configuration>
					<source>${java.version}</source>
					<target>${java.version}</target>
				</configuration>
			</plugin>

			<plugin>
					<groupId>org.sonarsource.scanner.maven</groupId>
					<artifactId>sonar-maven-plugin</artifactId>
					<version>3.0.2</version>

			</plugin>
		</plugins>
	</build>
```
4. Setup command line
<img width="1072" alt="Screen Shot 2019-11-07 at 9 00 09 AM" src="https://user-images.githubusercontent.com/37821007/68353766-209cc800-013d-11ea-8c89-babeded07034.png">
