## Tutorial Project for Automated Web Application Testing
### Description:
The framework uses the Page Object Model to test the site http://demowebshop.tricentis.com/.
### Framework structure
![Image alt](https://github.com/Mirents/ui_test_framework/raw/main/src/test/resources/SchemeFramework.jpg)
### Applied technology:
- Language: Java 1.8
- Build Automation Tool: Maven
- Frameworks: JUnit 5
- Logger: Log4j2 with Slf4j
- Drivers used: Selenium
- Test website: http://demowebshop.tricentis.com/
### Features:
- Separating Test Implementation and Test Specification
- Separating fixtures from tests
- Separating BOM layers
- Launching the browser in normal and non-graphical mode
- Run on Unix and Windows operating systems
- Element highlighting when interacting
### Installation and launch
- Copy the repository
- Add project to IDE
- Run command:
```sh
mvn test
```
To run tests on Unix, you need to run the command for the "/unix/chromedriver" file:
```sh
chmod u+x chromedriver
```
### Settings
Test run settings are located in the "application.properties" file located in:
"src/test/resources/"application.properties"
- "app.url" - Test site url address
- "browser.is.headless" - Non-graphical mode (yes/no)
- "browser.maximize.window" - Maximize window to full screen (yes/no)
- "browser.delete.all.cookies.before.start.tests" - Clearing cookies before starting (yes/no)
- "driver.implicity.wait" - Timeout for execution of actions in seconds
- "driver.page.load.timeout" - Page load timeout in seconds
- "wait.timeoutinseconds" - Wait element timeout in seconds
- "wait.sleepinmillis" - Wait element action timeout in milliseconds
- "higlilights.elements.enable" - Turn on element highlighting (yes/no)
- "higlilights.elements.count" - Number of flashes
- "higlilights.elements.interval" - Flash interval in milliseconds
- "higlilights.elements.color" - Flash color (HEX)
- "path.windows" - Root folder "src" for Windiws
- "path.unix" - Root folder "src" for Unix
- "path.driver.chrome.windows" - The folder of the web driver for Windows relative to the "src" folder
- "path.driver.chrome.unix" - The folder of the web driver for Unix relative to the "src" folder
### For reference
Browser driver included: ChromeDriver 97.0.4692.71.

The browser driver is located in the folder: 
- to Windows - "src/test/resources/drivers/windows/chromedriver.exe"
- to Unix - "src/test/resources/drivers/unix/chromedriver"

### Note
In a real framework project, highlighting can cause tests to fail when there is a viewport-blocking element.

To draw the diagram, the following was used: [yEd Graph Editor](https://www.yworks.com/products/yed)
