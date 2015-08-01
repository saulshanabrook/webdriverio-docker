# Webdriver Docker Exmaple

I can't get webdriver to connect to selenium in Docker. I keep getting a
`Couldn't connect to selenium server` error.

You can reproduce this error if you clone this repo and run `docker-compose up test-chrome`.

It also breaks with the same error using firefox or phantomjs. To run those
try `docker-compose up test-firefox` and `docker-compose up test-phantomjs`

The output I got was this:


```
$ docker-compose up test-chrome
webdriveriodocker_selenium-chrome_1 is up-to-date
Creating webdriveriodocker_test-chrome_1...
Attaching to webdriveriodocker_selenium-chrome_1, webdriveriodocker_test-chrome_1
selenium-chrome_1 | 11:40:42.211 INFO - Launching a standalone Selenium Server
selenium-chrome_1 | 11:40:42.285 INFO - Java: Oracle Corporation 24.79-b02
selenium-chrome_1 | 11:40:42.285 INFO - OS: Linux 4.0.7-boot2docker amd64
selenium-chrome_1 | 11:40:42.317 INFO - v2.46.0, with Core v2.46.0. Built from revision 87c69e2
selenium-chrome_1 | 11:40:42.467 INFO - Driver provider org.openqa.selenium.ie.InternetExplorerDriver registration is skipped:
selenium-chrome_1 | registration capabilities Capabilities [{platform=WINDOWS, ensureCleanSession=true, browserName=internet explorer, version=}] does not match the current platform LINUX
selenium-chrome_1 | 11:40:42.467 INFO - Driver class not found: com.opera.core.systems.OperaDriver
selenium-chrome_1 | 11:40:42.468 INFO - Driver provider com.opera.core.systems.OperaDriver is not registered
selenium-chrome_1 | 11:40:42.638 INFO - RemoteWebDriver instances should connect to: http://127.0.0.1:4444/wd/hub
selenium-chrome_1 | 11:40:42.638 INFO - Selenium Server is up and running
selenium-chrome_1 | 11:40:43.475 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5416ee46, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:40:43.519 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5416ee46, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 24620
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:40:46.101 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5416ee46, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
selenium-chrome_1 | 11:40:46.275 INFO - Executing: [delete session: 963ea5b4-43f4-471e-b3a5-1146fcf8b660])
selenium-chrome_1 | 11:40:46.841 INFO - Done: [delete session: 963ea5b4-43f4-471e-b3a5-1146fcf8b660]
selenium-chrome_1 | 11:41:04.629 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@45e30bcf, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:41:04.631 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@45e30bcf, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 22589
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:41:05.648 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@45e30bcf, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
selenium-chrome_1 | 11:41:05.840 INFO - Executing: [delete session: f10b95b1-7b7f-49d5-bb55-ee8aacc97958])
selenium-chrome_1 | 11:41:06.409 INFO - Done: [delete session: f10b95b1-7b7f-49d5-bb55-ee8aacc97958]
selenium-chrome_1 | 11:45:20.569 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@22623a55, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:45:20.570 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@22623a55, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 23942
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:45:21.441 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@22623a55, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
selenium-chrome_1 | 11:45:21.565 INFO - Executing: [delete session: d2e965f5-cd0d-4916-8892-a494c671beb9])
selenium-chrome_1 | 11:45:22.125 INFO - Done: [delete session: d2e965f5-cd0d-4916-8892-a494c671beb9]
selenium-chrome_1 | 11:46:12.502 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5cf3eac0, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:46:12.503 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5cf3eac0, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 11260
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:46:30.540 INFO - Launching a standalone Selenium Server
selenium-chrome_1 | 11:46:30.601 INFO - Java: Oracle Corporation 24.79-b02
selenium-chrome_1 | 11:46:30.602 INFO - OS: Linux 4.0.7-boot2docker amd64
selenium-chrome_1 | 11:46:30.632 INFO - v2.46.0, with Core v2.46.0. Built from revision 87c69e2
selenium-chrome_1 | 11:46:30.728 INFO - Driver provider org.openqa.selenium.ie.InternetExplorerDriver registration is skipped:
selenium-chrome_1 | registration capabilities Capabilities [{platform=WINDOWS, ensureCleanSession=true, browserName=internet explorer, version=}] does not match the current platform LINUX
selenium-chrome_1 | 11:46:30.729 INFO - Driver class not found: com.opera.core.systems.OperaDriver
selenium-chrome_1 | 11:46:30.729 INFO - Driver provider com.opera.core.systems.OperaDriver is not registered
selenium-chrome_1 | 11:46:30.826 INFO - RemoteWebDriver instances should connect to: http://127.0.0.1:4444/wd/hub
selenium-chrome_1 | 11:46:30.827 INFO - Selenium Server is up and running
selenium-chrome_1 | 11:46:32.694 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@167e6fb2, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:46:32.717 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@167e6fb2, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 5412
selenium-chrome_1 | Only local connections are allowed.
test-chrome_1     |
test-chrome_1     |
test-chrome_1     | =======================================================================================
test-chrome_1     | Selenium 2.0/webdriver protocol bindings implementation with helper commands in nodejs.
test-chrome_1     | For a complete list of commands, visit http://webdriver.io/docs.html.
test-chrome_1     | =======================================================================================
test-chrome_1     |
test-chrome_1     | [18:47:09]:  COMMAND    POST     "/wd/hub/session"
test-chrome_1     | [18:47:09]:  DATA        {"desiredCapabilities":{"browserName":"chrome","version":"","javascriptEnabled":true,"locationContextEnabled":true,"handlesAlerts":true,"rotatable":true,"platform":"ANY","loggingPrefs":{"driver":"INFO","browser":"INFO"},"requestOrigins":{"url":"http://webdriver.io","version":"3.1.0","name":"webdriverio"}}}
selenium-chrome_1 | 11:47:09.209 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5e36ba3b, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:47:09.210 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5e36ba3b, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 20182
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:47:10.145 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5e36ba3b, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
test-chrome_1     | [18:47:10]:  SET SESSION ID 4440cd89-34d1-4342-864a-5f2bb9e542d6
test-chrome_1     | [18:47:10]:  RESULT      {"platform":"LINUX","acceptSslCerts":true,"javascriptEnabled":true,"browserName":"chrome","chrome":{"userDataDir":"/tmp/.com.google.Chrome.1gVaZn"},"rotatable":false,"locationContextEnabled":true,"mobileEmulationEnabled":false,"webdriver.remote.sessionid":"4440cd89-34d1-4342-864a-5f2bb9e542d6","version":"43.0.2357.134","takesHeapSnapshot":true,"cssSelectorsEnabled":true,"databaseEnabled":false,"handlesAlerts":true,"browserConnectionEnabled":false,"nativeEvents":true,"webStorageEnabled":true,"hasTouchScreen":false,"applicationCacheEnabled":false,"takesScreenshot":true}
test-chrome_1     | my webdriverio tests
  1) "before all" hook
test-chrome_1     | [18:47:10]:  COMMAND    DELETE   "/wd/hub/session/4440cd89-34d1-4342-864a-5f2bb9e542d6"
test-chrome_1     | [18:47:10]:  DATA        {}
selenium-chrome_1 | 11:47:10.275 INFO - Executing: [delete session: 4440cd89-34d1-4342-864a-5f2bb9e542d6])
selenium-chrome_1 | 11:47:10.838 INFO - Done: [delete session: 4440cd89-34d1-4342-864a-5f2bb9e542d6]
test-chrome_1     |
test-chrome_1     |
test-chrome_1     | 0 passing (2.20s)
test-chrome_1     | 1 failing
test-chrome_1     |
test-chrome_1     | 1) "before all" hook:
test-chrome_1     | Couldn't connect to selenium server
test-chrome_1     | running chrome
test-chrome_1     | Error: Couldn't connect to selenium server
test-chrome_1     |     at Socket.socketErrorListener (_http_client.js:271:9)
test-chrome_1     |     at net.js:459:14
test-chrome_1     |
test-chrome_1     |
test-chrome_1     |
webdriveriodocker_test-chrome_1 exited with code 1
Gracefully stopping... (press Ctrl+C again to force)
```


You can see that it is reaching the selenium server but not working.
