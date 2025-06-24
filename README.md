# FlutterFlow Integration Tests Composite Action

This action will run the integration tests on flutterflow automatically. Note, I would recommend against swtiching the device from anything besides 'chrome', as whenever I tried, it failed. No argument is required, they all have default values. Also, by default, the flutter version is 3.27.3.

### Example Usage

```yaml

on: [push]
jobs:
  integration-test:
    runs-on: ubuntu-latest
    name: Integration Tests
    steps:
      - name: Test Integration Tests
        uses: flutterflow-integration-tests-action@master
      - name: After action
        run: |
          echo "Hello World!"
``` 

### Arguments

| Argument | Description | Default Value |
| --- | --- | --- |
| flutter-version | The current version of Flutter that FlutterFlow is using | 3.27.3 |
| test_path | The path where the actual tests are | integration_test/integration_test.dart |
| test_driver_path | The path to the setup of the tests | test_driver/integration_test.dart |
| chrome_driver_port | The port where chromedriver will be started in case you need it | 4444 |
| target_device | Target device to run the test on (chrome, web_server, android ...) | chrome |

