# Spring Boot Rest API development:

## Running Spring Boot Application locally

You can test the rest API's locally using the below curl commands.

1. To get the list of users:
```
curl --location --request GET 'http://localhost:8081/users'
```

2. Create user:
```
curl --location --request POST 'http://localhost:8081/users' \
--header 'Content-Type: application/json' \
--data-raw '{
    "userName": "user 7",
    "userEmail": "user7@gmail.com"
}
```

3. Update user
```
curl --location --request PUT 'http://localhost:8081/users/10' \
--header 'Content-Type: application/json' \
--data-raw '{
    "userName": "user 7",
    "userEmail": "user07@gmail.com"
}'
```

4. Delete user
```
curl --location --request DELETE 'http://localhost:8081/users/10' \
--data-raw ''
```

 
## Working with Spring Boot RestApi

### Prerequisites
The following items should be installed in your system:
* Spring Tool Suite or any of your favourite tool
* MySQL server & MySql workbench
* Git
* Maven


### Technology Used:     
  Java 8                                                                                                                                
  Spring Boot & Spring Framework                                                                                                                           
  JPA & Hibernate     
  Junit and Mockito    
  Sonarqube                                                                                                                  
                                                                                                                           
 
### Steps to Clone The Repository Application:

1) Download this Project from Git.
```
git clone https://github.com/Sudarshan-Gowda/spring-boot-all-in-one.git
```
2) To Import the Project in your development tool.
```
File -> Import -> Maven -> Existing Maven project -> spring-boot-all-in-one
```
3) Checkout to branch using cmd
```
git checkout Sonaqube-scanning-using-properties-file
```

## Steps to test the application:

### To Run the Spring Boot Application:
`step 1`: Download this repository & do maven import.    
`step 2`: Go to the main class file and run as Spring boot application. <br>
`step 3`: Once the application is successfully started, It can be accessed by using url `http://localhost:8081`

## Steps to Setup and run the Sonaqube reports:
There are multiple sites available in the Internet to download and setup the sonarqube. 

If you are using macos you can make use of this site:
https://techblost.com/how-to-setup-sonarqube-locally-on-mac/

To read the properties from sonar-project.properties for sonaqube scanning, replace the Auth Id of yours for the property key `sonar.login` in the `sonar-project.properties` file and execute the below commands.

```
mvn clean install
sonar-scanner
```

1. mvn clean install : this will generate the jacoco report under target folder based the plugin added in the pox.xml
2. sonar-scanner     : this will read the configuration from sonar-project.properties file and generate the dashboard in sonaqube with coverage detail.

After executing above commands you should be able to see the below success message in your terminal.

<img src="/docs/Pic-01.png" width="100%" height="100%">


You can navigate to sonaqube dashboard in the browser using `http://localhost:9000/`

<img src="/docs/Pic-02.png" width="100%" height="100%">



# Contributing

The [issue tracker](https://github.com/Sudarshan-Gowda/spring-boot-all-in-one/issues) is the preferred channel for bug reports, features requests and submitting pull requests.

