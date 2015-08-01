# Webdriver Docker Exmaple

I can't get webdriver to connect to selenium in Docker. I keep getting a
`Couldn't connect to selenium server` error.

You can reproduce this error if you clone this repo and run `docker-compose up`.

The output I got was this:


```
$ docker-compose up
Removing webdriveriodocker_test_1...
Starting webdriveriodocker_selenium-chrome_1...
Recreating fa78d926f6_fa78d926f6_webdriveriodocker_test_1...
Attaching to webdriveriodocker_selenium-chrome_1, webdriveriodocker_test_1
selenium-chrome_1 | 11:06:19.775 INFO - Launching a standalone Selenium Server
selenium-chrome_1 | 11:06:19.856 INFO - Java: Oracle Corporation 24.79-b02
selenium-chrome_1 | 11:06:19.856 INFO - OS: Linux 4.0.7-boot2docker amd64
selenium-chrome_1 | 11:06:19.893 INFO - v2.46.0, with Core v2.46.0. Built from revision 87c69e2
selenium-chrome_1 | 11:06:20.033 INFO - Driver provider org.openqa.selenium.ie.InternetExplorerDriver registration is skipped:
selenium-chrome_1 | registration capabilities Capabilities [{platform=WINDOWS, ensureCleanSession=true, browserName=internet explorer, version=}] does not match the current platform LINUX
selenium-chrome_1 | 11:06:20.034 INFO - Driver class not found: com.opera.core.systems.OperaDriver
selenium-chrome_1 | 11:06:20.034 INFO - Driver provider com.opera.core.systems.OperaDriver is not registered
selenium-chrome_1 | 11:06:20.181 INFO - RemoteWebDriver instances should connect to: http://127.0.0.1:4444/wd/hub
selenium-chrome_1 | 11:06:20.181 INFO - Selenium Server is up and running
selenium-chrome_1 | xvfb-run: error: Xvfb failed to start
selenium-chrome_1 | xvfb-run: error: Xvfb failed to start
selenium-chrome_1 | xvfb-run: error: Xvfb failed to start
selenium-chrome_1 | 11:07:50.157 INFO - Launching a standalone Selenium Server
selenium-chrome_1 | 11:07:50.210 INFO - Java: Oracle Corporation 24.79-b02
selenium-chrome_1 | 11:07:50.211 INFO - OS: Linux 4.0.7-boot2docker amd64
selenium-chrome_1 | 11:07:50.231 INFO - v2.46.0, with Core v2.46.0. Built from revision 87c69e2
selenium-chrome_1 | 11:07:50.330 INFO - Driver provider org.openqa.selenium.ie.InternetExplorerDriver registration is skipped:
selenium-chrome_1 | registration capabilities Capabilities [{platform=WINDOWS, ensureCleanSession=true, browserName=internet explorer, version=}] does not match the current platform LINUX
selenium-chrome_1 | 11:07:50.330 INFO - Driver class not found: com.opera.core.systems.OperaDriver
selenium-chrome_1 | 11:07:50.330 INFO - Driver provider com.opera.core.systems.OperaDriver is not registered
selenium-chrome_1 | 11:07:50.429 INFO - RemoteWebDriver instances should connect to: http://127.0.0.1:4444/wd/hub
selenium-chrome_1 | 11:07:50.429 INFO - Selenium Server is up and running
selenium-chrome_1 | 11:08:41.504 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@782be176, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:08:41.527 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@782be176, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 8517
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:08:43.737 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@782be176, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
selenium-chrome_1 | 11:08:43.773 INFO - Executing: [delete session: 139f53ad-c1fa-41ee-b715-181fbd545de1])
selenium-chrome_1 | 11:08:44.337 INFO - Done: [delete session: 139f53ad-c1fa-41ee-b715-181fbd545de1]
selenium-chrome_1 | 11:09:39.200 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5367839e, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:09:39.202 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5367839e, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 29954
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:09:40.101 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5367839e, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
selenium-chrome_1 | 11:09:58.422 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@30848636, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:09:58.424 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@30848636, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 4002
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:10:35.916 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5af3a6eb, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:10:35.917 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5af3a6eb, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 31357
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:10:36.882 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@5af3a6eb, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
selenium-chrome_1 | 11:11:31.178 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@14d21a89, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:11:31.180 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@14d21a89, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 18459
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:12:49.189 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@36b93e8f, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:12:49.191 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@36b93e8f, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 8235
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:12:50.202 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@36b93e8f, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
selenium-chrome_1 | 11:13:12.088 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@6069094, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:13:12.090 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@6069094, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 14920
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:13:13.029 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@6069094, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
selenium-chrome_1 | 11:13:44.918 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@1a96fdd7, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:13:44.919 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@1a96fdd7, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 31355
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:13:45.806 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@1a96fdd7, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
selenium-chrome_1 | 11:13:48.781 INFO - Executing: [delete session: f6a5b72f-8db6-4f47-a721-c51a3196814d])
selenium-chrome_1 | 11:13:49.339 INFO - Done: [delete session: f6a5b72f-8db6-4f47-a721-c51a3196814d]
selenium-chrome_1 | 11:14:04.170 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@1c8e8f1e, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:14:04.171 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@1c8e8f1e, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 23964
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:14:05.043 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@1c8e8f1e, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
selenium-chrome_1 | 11:14:07.710 INFO - Executing: [delete session: 51d001f6-adb3-46f3-87a0-706cdc49753d])
selenium-chrome_1 | 11:14:08.268 INFO - Done: [delete session: 51d001f6-adb3-46f3-87a0-706cdc49753d]
selenium-chrome_1 | 11:14:28.206 INFO - Launching a standalone Selenium Server
selenium-chrome_1 | 11:14:28.316 INFO - Java: Oracle Corporation 24.79-b02
selenium-chrome_1 | 11:14:28.316 INFO - OS: Linux 4.0.7-boot2docker amd64
selenium-chrome_1 | 11:14:28.337 INFO - v2.46.0, with Core v2.46.0. Built from revision 87c69e2
selenium-chrome_1 | 11:14:28.499 INFO - Driver provider org.openqa.selenium.ie.InternetExplorerDriver registration is skipped:
selenium-chrome_1 | registration capabilities Capabilities [{platform=WINDOWS, ensureCleanSession=true, browserName=internet explorer, version=}] does not match the current platform LINUX
selenium-chrome_1 | 11:14:28.499 INFO - Driver class not found: com.opera.core.systems.OperaDriver
selenium-chrome_1 | 11:14:28.499 INFO - Driver provider com.opera.core.systems.OperaDriver is not registered
selenium-chrome_1 | 11:14:28.633 INFO - RemoteWebDriver instances should connect to: http://127.0.0.1:4444/wd/hub
selenium-chrome_1 | 11:14:28.633 INFO - Selenium Server is up and running
test_1            |
test_1            |
test_1            | =======================================================================================
test_1            | Selenium 2.0/webdriver protocol bindings implementation with helper commands in nodejs.
test_1            | For a complete list of commands, visit http://webdriver.io/docs.html.
test_1            | =======================================================================================
test_1            |
test_1            | [18:14:29]:  COMMAND    POST     "/wd/hub/session"
test_1            | [18:14:29]:  DATA        {"desiredCapabilities":{"browserName":"chrome","version":"","javascriptEnabled":true,"locationContextEnabled":true,"handlesAlerts":true,"rotatable":true,"platform":"ANY","loggingPrefs":{"driver":"INFO","browser":"INFO"},"requestOrigins":{"url":"http://webdriver.io","version":"3.1.0","name":"webdriverio"}}}
selenium-chrome_1 | 11:14:29.784 INFO - Executing: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@2fa956c0, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]])
selenium-chrome_1 | 11:14:29.804 INFO - Creating a new session for Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@2fa956c0, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]
selenium-chrome_1 | Starting ChromeDriver 2.16.333243 (0bfa1d3575fc1044244f21ddb82bf870944ef961) on port 18897
selenium-chrome_1 | Only local connections are allowed.
selenium-chrome_1 | 11:14:30.940 INFO - Done: [new session: Capabilities [{loggingPrefs=org.openqa.selenium.logging.LoggingPreferences@2fa956c0, platform=ANY, javascriptEnabled=true, handlesAlerts=true, browserName=chrome, requestOrigins={name=webdriverio, url=http://webdriver.io, version=3.1.0}, rotatable=true, locationContextEnabled=true, version=}]]
test_1            | [18:14:30]:  SET SESSION ID 42178572-08f3-4363-a54e-6ef69dda102c
test_1            | [18:14:30]:  RESULT      {"platform":"LINUX","acceptSslCerts":true,"javascriptEnabled":true,"browserName":"chrome","chrome":{"userDataDir":"/tmp/.com.google.Chrome.nHGUAc"},"rotatable":false,"locationContextEnabled":true,"mobileEmulationEnabled":false,"webdriver.remote.sessionid":"42178572-08f3-4363-a54e-6ef69dda102c","version":"43.0.2357.134","takesHeapSnapshot":true,"cssSelectorsEnabled":true,"databaseEnabled":false,"handlesAlerts":true,"browserConnectionEnabled":false,"nativeEvents":true,"webStorageEnabled":true,"hasTouchScreen":false,"applicationCacheEnabled":false,"takesScreenshot":true}
test_1            | my webdriverio tests
  1) "before all" hook
test_1            | [18:14:34]:  COMMAND    DELETE   "/wd/hub/session/42178572-08f3-4363-a54e-6ef69dda102c"
test_1            | [18:14:34]:  DATA        {}
selenium-chrome_1 | 11:14:34.227 INFO - Executing: [delete session: 42178572-08f3-4363-a54e-6ef69dda102c])
selenium-chrome_1 | 11:14:34.791 INFO - Done: [delete session: 42178572-08f3-4363-a54e-6ef69dda102c]
test_1            |
test_1            |
test_1            | 0 passing (6.00s)
test_1            | 1 failing
test_1            |
test_1            | 1) "before all" hook:
test_1            | Couldn't connect to selenium server
test_1            | running chrome
test_1            | Error: Couldn't connect to selenium server
test_1            |     at Socket.socketErrorListener (_http_client.js:271:9)
test_1            |     at net.js:459:14
test_1            |
test_1            |
test_1            |
webdriveriodocker_test_1 exited with code 1
Gracefully stopping... (press Ctrl+C again to force)
Stopping webdriveriodocker_selenium-chrome_1... done
```


You can see that it is reaching the selenium server but not working.
