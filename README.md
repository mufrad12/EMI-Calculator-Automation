# EMI-Calculator-Automation

# Appium Basic Google Calculator Automation
### This is an automation on EMI calculator app with Selenium Appium. 
EMI Calculator is simple loan calculation tool that helps user to quickly calculate EMI and view payment schedule. Use this app to calculate your EMI (Equated Monthly Instalment), plan your loan repayment in effective way. This app is the advanced Financial Tool that is useful for day to day life with all useful features and keep upto date with the latest news.

### Technology: </br>
- Tool: Selenium Webdriver
- IDE: Intellij, Android Studio
- Build tool: Gradle
- Language: Java
- Test_Runner: Appium


## Scenerio:
If an user take loan (?) tk from a bank with interest of (?)% and  want to give (?) tk per month as EMI (installment) and processing fee (?)%, how many time period it will take to complete the loan? Take the values from dataset and assert the monthly EMI, total interest, processing fee amount and total payment from the result view. (See below image)

For solve this question, create a dataset using following values:

Amount | Interest | EMI | Processing Fee | Monthly EMI | Total Interest | Processing Fee | Total Payment | Period (Year) | Period (Month)

100000 | 6 | 2000 | 2% | 2000 | 15361.08 | 2000 | 115361.08 | 4 | 10
200000 | 8 | 5000 | 2% | 5000 | 33391.61 | 4000 | 233391.61 | 3 | 11

250000 | 7 | 8000 | 1.5% | 8000 | 26804.51 | 3750 | 276804.51 | 2 | 11

50000 | 10 | 1000 | 5% | 1000 | 14949.12 | 2500 | 64949.12 | 5 | 5

### Prerequisites</br>
- Install Android Studio latest version
- Install Appium 1.17.1
- Install jdk 8 or any LTS version

## How to run this project:

- Clone this project
- Open Android Studio and Open the APK file:
- Set required configuration 
- Hit this command in cmd for checking the connectivity with emulator : ``adb devices``
- Open Appium Server with following command: ```appium -p 4723```
- Open Appium Inspector
- Set desired capabilites in json format:
``` 
 {
 "appium:deviceName": "emulator",
  "appium:uuid": "emulator-5554",
  "platformName": "Android",
  "appium:platformVersion": "11",
  "appium:appPackage": "com.continuum.emi.calculator",
  "appium:appActivity": "com.finance.emicalci.activity.Splash_screnn",
  "appium:app": "D:\\RTSDET\\APK\\emi-calc.apk"
  }
```
- Open Intellij Idea
- Hit the following command into the terminal: ```gradle clean test```

- The following report is generated:

![Screenshot 2023-03-02 231256](https://user-images.githubusercontent.com/58912515/222506152-ad2d3195-c657-44cb-aba7-c98536586d80.png)


- After automation to view allure report , give the following commands:
 ```
allure generate allure-results --clean -o allure-report
allure serve allure-results
 ```
**Here is the Allure report overview:**
![Screenshot 2023-03-02 230042](https://user-images.githubusercontent.com/58912515/222506112-51dee7cc-649c-4f7a-a03d-cbbf8da11b60.png)

![Screenshot 2023-03-02 230054](https://user-images.githubusercontent.com/58912515/222506128-8ed7297a-52c4-42fb-85d2-0c7097b101ed.png)

##Automation Video Output:

https://user-images.githubusercontent.com/58912515/222795400-71fa9480-9e3a-40ff-acfd-0a155bba5b58.mp4














