# AutomationFramework_API-UI

--------------------------------------------------------------------------------------------
Demo: Hybrid Framework
--------------------------------------------------------------------------------------------
1. Requirement for new framework (Why?).
	- Combined where both UI and API testing can be achieved.
2. Tech-Stack Involved. 
	- Core Java, Cucumber BDD, Selenium WebDriver and API understanding.
3. Reporting: Generating test Results.
	- Cucumber Reporting -> Generate based on tags, specific tests
4. Advantages: Integration with Jenkins and Commands
	- POM based model for UI.
	- Nashorn : Advanced JS engine for validation of JSON response.
	- Easy maintainence as it's modularised.
	- Easy enhancement and pluggable as Maven project.

--------------------------------------------------------------------------------------------
To run both module's tests: 
$ mvn clean test

Approach 01: (Using advanced maven config.)
To run a specific module: 
$ mvn -pl Backend_Module -am clean test

Approach 02: (Using profile's)
$ mvn clean test -P apiTests

Run a specific test:
$ mvn clean test -P apiTests -Dcucumber.options="src/test/java/examples/users/usersAdvanced.feature"
$ mvn clean test -P apiTests -DargLine="-Dkarate.env=e2e"

$ mvn test -Dcucumber.options='--tags "@smoke and @fast"'
------------------------------------------------------------------------------------------------

Environment set-up for API's: 
For setting up diff environments: (In Karate-config.json, Invoke from Command Line)s

Semaphore: https://semaphoreci.com/community/tutorials/testing-a-java-spring-boot-rest-api-with-karate

Reporting: https://stackoverflow.com/questions/45641603/no-html-reports-in-my-target-folder
Community links with video : https://github.com/intuit/karate/wiki/Community-News

https://github.com/intuit/karate#http-basic-authentication-example
Calling a js with arguments.

with beautiful examples:
https://www.testingexcellence.com/karate-api-testing-tool-cheat-sheet/

https://github.com/intuit/karate#hooks 
to call a function Before, After etc..  Cucumber is having different hooks and Karate is different.
