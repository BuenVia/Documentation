# SELENIUM

A basic Selenium script

```python
from selenium import webdriver
from selenium.webdriver.common.by import By

# Keeps Chrome window open until end of script
chrome_options = webdriver.ChromeOptions()
chrome_options.add_experimental_option("detach", True)

# Define the driver and make GET requetes to specific site
driver = webdriver.Chrome(options=chrome_options)
driver.get("https://secure-retreat-92358.herokuapp.com/")

# Search for specific elements on page
fname = driver.find_element(By.NAME, "fName")
lname = driver.find_element(By.NAME, "lName")
email = driver.find_element(By.NAME, "email")
submit = driver.find_element(By.CLASS_NAME, "form-signin button")

# DDefine actions on the elements found on page
fname.send_keys("Matthew")
lname.send_keys("Clifford")
email.send_keys("matthewclifford@hotmail.co.uk")
submit.click()

# driver.quit()
```
