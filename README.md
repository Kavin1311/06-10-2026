```
import time
from selenium import webdriver 
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import Select

driver = webdriver.Edge()
driver.get("https://vinothqaacademy.com/demo-site/")
time.sleep(10)
driver.find_element(By.ID, "vfb-5").send_keys("Kavin")
driver.find_element(By.ID, "vfb-7").send_keys("Ajai")

driver.find_element(By.ID, "vfb-31-1").click()
driver.find_element(By.ID, "vfb-20-0").click()

street_address = driver.find_element(By.ID, "vfb-13-address")
street_address.clear()
street_address.send_keys("123 Main Street")

apt_suite = driver.find_element(By.ID, "vfb-13-address-2")
apt_suite.clear()
apt_suite.send_keys("Apt 4B")

city = driver.find_element(By.ID, "vfb-13-city")
city.clear()
city.send_keys("New York")

state = driver.find_element(By.ID, "vfb-13-state")
state.clear()
state.send_keys("NY")

zip_code = driver.find_element(By.ID, "vfb-13-zip")
zip_code.clear()
zip_code.send_keys("10001")

country_dropdown = Select(driver.find_element(By.ID, "vfb-13-country"))
country_dropdown.select_by_visible_text("United States of America")

email = driver.find_element(By.ID, "vfb-14")
email.clear()
email.send_keys("test@example.com")

demo_date = driver.find_element(By.ID, "vfb-18")
demo_date.clear()
demo_date.send_keys("10/25/26")

hours_dropdown = Select(driver.find_element(By.ID, "vfb-16-hour"))
hours_dropdown.select_by_value("10")

minutes_dropdown = Select(driver.find_element(By.ID, "vfb-16-min"))
minutes_dropdown.select_by_value("30")

mobile = driver.find_element(By.ID, "vfb-19")
mobile.clear()	
mobile.send_keys("9876543210")

query = driver.find_element(By.ID, "vfb-23")
query.clear()
query.send_keys("Please provide details about the course syllabus")
driver.find_element(By.ID,"vfb-4").click()

time.sleep(10)
driver.quit()
```
## What this code does:

Here’s a clean **GitHub-ready description** you can copy-paste:

### Selenium Demo Form Automation

* Automated the **Vinoth QA Academy Demo Form** using **Selenium WebDriver with Python**.
* Launched the website using **Microsoft Edge WebDriver**.
* Entered **first name** and **last name**.
* Selected required **radio buttons/checkboxes**.
* Filled in **street address, apartment/suite, city, state, and ZIP code**.
* Selected **country** from a dropdown using Selenium's `Select` class.
* Entered and validated an **email address**.
* Entered a **demo date**.
* Selected **hour and minute** from dropdown menus.
* Entered a **mobile number**.
* Filled the **query/message field** with a course-related question.
* Located form elements using Selenium **ID locators**.
* Used Selenium methods such as `send_keys()`, `clear()`, and `click()`.
* Used `Select` for handling **HTML dropdown elements**.
* Submitted the completed form automatically.
* Added delays using `time.sleep()` to allow the page and form actions to complete.
* Closed the browser using `driver.quit()` after execution.

**Technologies Used:**
`Python` | `Selenium WebDriver` | `Microsoft Edge` | `HTML Form Automation` | `Web Element Locators` | `Dropdown Handling`
