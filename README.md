# Importing necessary libraries
from selenium import webdriver

# Initializing the Chrome webdriver
driver = webdriver.Chrome()

# Navigating to the URL
driver.get("https://www.instagram.com/guviofficial/")

# Extracting the total number of followers using XPath
followers = driver.find_element_by_xpath("//a[@href='/guviofficial/followers/']/span")
total_followers = followers.get_attribute('title')
print("Total Followers:", total_followers)

# Extracting the total number of following using XPath
following = driver.find_element_by_xpath("//a[@href='/guviofficial/following/']/span")
total_following = following.text
print("Total Following:", total_following)

# Closing the browser window
driver.close()
