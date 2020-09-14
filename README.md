Project Title
Travel website-Flight search function

Introduction
Selenium TestNG Framework (Maven Project)
This is a page object model design pattern.

Getting Started
Selenium Java Testng project for  automation Travel website-Flight search function
Test source files are in src\test\java
Driver is loaded using factory
Logging added with Log4j
Config files are used
Test can be run as a suite using Maven
In this project I used Maven, testng and log4j is used for logging.
Selenium-TestNG-Framework
#Install
Clone and import the project as existing Maven project in any Java IDE. 
you can run the program using any IDE like Eclipse or IntelliJ or from Jenkins but Ensure Maven plugin is available. 
Update \src\test\resources\config.properties file, property 'driver.location' with your browser driver(Chrome) location
Run Maven Install to run up to tests

How to use

src/main/java
Base package( com.thinkbridge.Base)
Use of this package is to set all requirements of data in this class.

listener package ( com.thinkbridge.listener) TestNG Listner
Use of this package is to listen any operation/event that happened during any execution. for this TestNG listner methods like onstart,onfinish,ontestpassed, onTestskipped etc are overwritten. Listener and Reporter has to be implement jointly and in a planned manner as per the requirement. So few sample features are implemented in this project. Please open a case if you require more assistance in Listener and Reporter package/functionality.

Page Object Package (com.thinkbride.page)
This package is used for modelling of page objects. various page objects are stored as By class objects which will be used by testscripts and page wise reuseable code. 
[Note] - Inplace of locators being stored as By Class object i have stored them as string in format "LocatorType==Locator". Example "xpath==.//*[@id='gb_70']" or "id==lst-ib" . Here locator type is id and Locator is lst-ib. 
 benefit of this method is that we can store the locator in other places also in same format as string or key-value pair. So to accomodate this change. code just before the findelement method(selenium method which identify the object in the page) has a string split using "==" and pass then pass the locator to it. you can return back to the page object by using BY object method and little modification of findelement method in seleniumrepo package.

src/test/java
Test package( com.thinkbridge.test)
This package is used to test the test class file.

src/test/resources
log4j.properties - used to generate logs
ObjectRepository.properties - used to store data related with the project.

tets-output folder
TestNGReport - emailable-report.html - This is report used to see status of the TestCases.
pom.xml - used to store all dependencies for project
testng.xml - for running tetsSuite in xml.

Versioning
I used Git for versioning.
