# Saucedemo
SauceDemo Automated Test – Add Highest Price Item to Cart
This project demonstrates an automated UI test using Selenium WebDriver with JUnit for testing the SauceDemo web application. The test logs in with a standard user, identifies the product with the highest price, adds it to the shopping cart, and verifies that the cart badge reflects the addition.
Prerequisites

Before running the tests, ensure you have the following installed:

Java JDK 8 or higher
Maven (for dependency management)
Google Chrome browser
Internet connection (for WebDriverManager to download drivers)
The project uses:
Selenium WebDriver – for browser automation
JUnit – for test management and assertions
WebDriverManager – automatically manages browser drivers
Setup
Clone or download the repository.
Add the following dependencies in pom.xml if using Maven:

<dependencies>
    <dependency>
        <groupId>org.seleniumhq.selenium</groupId>
        <artifactId>selenium-java</artifactId>
        <version>4.12.1</version>
    </dependency>
    <dependency>
        <groupId>io.github.bonigarcia</groupId>
        <artifactId>webdrivermanager</artifactId>
        <version>5.5.0</version>
    </dependency>
    <dependency>
        <groupId>junit</groupId>
        <artifactId>junit</artifactId>
        <version>4.13.2</version>
    </dependency>
</dependencies>


Ensure Chrome is installed and up-to-date.
Build the project using Maven:
mvn clean install

Project Structure
src/test/java/
└── LoginScenarioTest.java  # Main test class
LoginScenarioTest.java includes:
setUp() – initializes the Chrome browser before tests
login() – reusable method for logging in
addHighestPriceItemToCart() – finds and adds the product with the highest price
testAddHighestPriceItemToCart() – main test case with verification
cleanUp() – closes the browser after tests
Test Workflow
Launch Chrome browser using WebDriverManager.
Navigate to SauceDemo
Log in using credentials:
Username: standard_user
Password: secret_sauce

Scan all product prices on the inventory page.
Identify the product with the highest price.
Click the Add to Cart button for that product.
Verify that the shopping cart badge shows 1.
Close the browser.
Running the Test
Navigate to the project directory.
Run the test using Maven:
mvn test

Highest price item added: $49.99
