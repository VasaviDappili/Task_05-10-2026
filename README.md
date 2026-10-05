# Task_05-10-2026

# Swag Labs

## Code
```
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()

driver.get("https://www.saucedemo.com/")

username = driver.find_element(By.ID, "user-name")
password = driver.find_element(By.NAME, "password")
login = driver.find_element(By.ID, "login-button")

username.send_keys("standard_user")
password.send_keys("secret_sauce")

print(username.get_attribute("placeholder"))
print(login.is_enabled())
print(username.is_displayed())
input("Press Enter to close the browser...")

driver.quit()
```

## Output

<img width="1917" height="1018" alt="image" src="https://github.com/user-attachments/assets/96637662-e7f3-4720-a1f4-9f013bbbda02" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7da31f5e-5d16-4d60-88ba-35953b2c56e5" />
<img width="1917" height="1020" alt="image" src="https://github.com/user-attachments/assets/f275bc4e-0029-43b1-aea5-7b34c92397a2" />
<img width="1917" height="1022" alt="image" src="https://github.com/user-attachments/assets/50161de8-f72e-4b7f-b6cf-4cca5d0bd5a9" />
<img width="1917" height="1023" alt="image" src="https://github.com/user-attachments/assets/d48a5ca9-39bd-4619-b322-40d95c534490" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6da493e2-0d9c-4334-a290-73c926eae336" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c888c4a9-4de0-4d96-8bee-6400b14e251a" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/eb2fb60b-cc83-463b-939e-e2f3f3cda8a8" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/659f09e9-3b44-45e6-873c-be98624959a9" />



# Flipcart Login_Page

## Code
```
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import time


driver = webdriver.Chrome()
driver.maximize_window()


wait = WebDriverWait(driver, 30)


driver.get("https://www.flipkart.com/")

print("Flipkart opened successfully.")


login_button = wait.until(
    EC.presence_of_element_located(
        (By.XPATH, "//*[normalize-space()='Login']")
    )
)

print("Login button found.")


driver.execute_script(
    "arguments[0].scrollIntoView({block: 'center'});",
    login_button
)

time.sleep(1)


driver.execute_script(
    "arguments[0].click();",
    login_button
)

print("Login button clicked.")


mobile = wait.until(
    EC.visibility_of_element_located(
        (By.XPATH, "//input[@type='text' or @type='tel']")
    )
)

print("Mobile number field found.")


mobile.send_keys("YOUR_MOBILE_NUMBER")

print("Mobile number entered.")

print()
print("======================================")
print("Now click Request OTP manually.")
print("Enter the OTP manually in Chrome.")
print("Chrome will remain open.")
print("======================================")

input("Complete the login. Press ENTER when you want to close Chrome...")

driver.quit()
```

## Output

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/6065cb32-4072-425a-8238-ca0ddf3c9225" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2a59cb77-2940-4f9a-8a05-6422b05fcdcf" />
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/b1150ba9-1135-421b-b637-9a0b305a0926" />
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/5a01bedc-ee59-468b-8d20-3b251074b1fd" />


