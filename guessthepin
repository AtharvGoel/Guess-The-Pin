# guess the pin
# tries each number from 0 to 9999 on guessthepin.com till correct number is found.

from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get('https://guessthepin.com')

data = '0000'

while True:
    pin = driver.find_element(By.ID, 'pin')
    pin.send_keys(data)

    pin.submit()
    
    data = str(int(data) + 1)
    if len(data) != 4:
        data = '0'*(4-len(data)) + data
    elif data == '10000':
        data = '0000'
        
