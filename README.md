from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

# Open browser
driver = webdriver.Chrome()

# Open demo website
driver.get("https://the-internet.herokuapp.com/login")

# Maximize window
driver.maximize_window()

# Enter username
driver.find_element(By.ID, "username").send_keys("tomsmith")

# Enter password
driver.find_element(By.ID, "password").send_keys("SuperSecretPassword!")

# Click login
driver.find_element(By.CSS_SELECTOR, "button[type='submit']").click()

time.sleep(3)

# Close browser
driver.quit()
