# Testing Login Functionality with Selenium and Python

Selenium is a powerful tool for controlling a web browser through the program. It is functional for all browsers, works on all major operating systems, and is available in various languages such as Python, Java, C#, etc.

To test the login functionality of a webpage using Selenium in Python, you can use the following steps:

Install the Selenium Python library and the webdriver for your preferred browser. For example:
``` python
pip install selenium
```

Import the necessary Selenium modules and set up the webdriver:
```
from selenium import webdriver

# Replace with the path to your webdriver
driver = webdriver.Chrome('/path/to/chromedriver')
```

Navigate to the login page:
```pyhton
driver.get('https://www.example.com/login')
```

Find the elements for the username and password fields and enter the appropriate values:
```python
username_field = driver.find_element_by_id('username')
password_field = driver.find_element_by_id('password')

username_field.send_keys('your_username')
password_field.send_keys('your_password')
```

Find the login button and click it:

```python
login_button = driver.find_element_by_id('login_button')
login_button.click()
```

Test that the login was successful by checking for certain elements that should be present on the logged-in page, or by checking the URL of the current page:
```python
# Check for specific elements
profile_link = driver.find_element_by_id('profile_link')
assert profile_link.is_displayed()

# Check the current URL
assert driver.current_url == 'https://www.example.com/profile'
```

Close the webdriver when you're finished:
``` pyhton
driver.close()
```
This is just a basic example, and you can add additional features and error handling as needed for your specific use case.

<image src ="ScreenShots/A.png" width="800">

