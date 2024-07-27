# tmp-repo
```python
from selenium import webdriver
from selenium.webdriver.chrome.service import Service as ChromeService
from selenium.webdriver.common.by import By
from webdriver_manager.chrome import ChromeDriverManager
from selenium.webdriver.common.action_chains import ActionChains
import time


driver = webdriver.Chrome(service=ChromeService(ChromeDriverManager().install()))

driver.get('https://sketchtoy.com/')
# driver.get('C:/DevStation/playground/index.html')
driver.maximize_window()


canvas = driver.find_element(By.XPATH, "//div[@class='sketch-canvas-container']/canvas")
# action = ActionChains(driver)

# Click and hold at the starting point (x, y) on the canvas
# action.move_to_element_with_offset(canvas, 50, 50).click_and_hold()

# action.move_by_offset(30, 10)
# action.move_by_offset(10, 20)
# action.move_by_offset(-20, 10)
# action.move_by_offset(-10, -20)
# action.move_by_offset(10, -30)

# # Release the mouse button to complete the drawing
# action.release()

# # Perform the actions
# action.perform()
# draw_signature_script = """
# var canvas = arguments[0];
# var ctx = canvas.getContext('2d');
# ctx.beginPath();
# ctx.moveTo(50, 50);  // Starting point
# ctx.lineTo(80, 60);
# ctx.lineTo(90, 80);
# ctx.lineTo(70, 90);
# ctx.lineTo(60, 70);
# ctx.lineTo(70, 40);
# ctx.stroke();
# """

# # Execute the JavaScript to draw on the canvas
# driver.execute_script(draw_signature_script, canvas)

# action = ActionChains(driver)

# Move to the starting point on the canvas
# action.move_to_element_with_offset(canvas, 30, 50).click_and_hold()

# Simulate drawing a complex signature
# You can adjust the offset values to create the desired signature shape
# movements = [
#     (10, 20), (20, -10), (30, 40), (40, -20), (50, 10),
#     (-20, -30), (-30, 20), (-40, 10), (20, -20), (30, 30)
# ]

# movements = [
#     # 'a'
#     (10, 10), (10, -20), (10, 10), (10, 10), (-10, 0), (-10, 10), (0, 10), (10, 10),
#     # 'u'
#     (20, -10), (0, -20), (10, 0), (10, 20), (0, -20), (10, 0),
#     # 't'
#     (20, -10), (0, 20), (10, -10), (-20, 0), (20, -10), (0, 20),
#     #'o'
#     (20, 0), (10, 10), (0, 20), (-10, 10), (-10, -10), (0, -20), (10, -10), (10, 10),
    # # 'm'
    # (20, 0), (0, 20), (10, -10), (10, 10), (0, -20), (10, 0), (10, 10), (0, 20),
    # # 'a'
    # (20, 0), (0, -20), (10, 10), (10, 10), (-10, 0), (-10, 10), (0, 10), (10, 10),
    # # 't'
    # (20, -10), (0, 20), (10, -10), (-20, 0), (20, -10), (0, 20),
    # # 'i'
    # (20, -10), (0, 20), (0, -10), (10, 0), (0, -10), (0, 20),
    # # 'o'
    # (20, 0), (10, 10), (0, 20), (-10, 10), (-10, -10), (0, -20), (10, -10), (10, 10),
    # # 'n'
    # (20, 0), (0, 20), (10, -10), (10, 10), (0, -20), (10, 0)
# ]

# # Draw the signature using the defined movements
# for move in movements:
#     action.move_by_offset(*move)

# # Release the mouse button to complete the drawing
# action.release()

# # Perform the actions
# action.perform()

# for move in movements:
#     action.move_by_offset(*move)

# # Release the mouse button to complete the drawing
# action.release()

# # Perform the actions
# action.perform()




# draw_signature_script = """
# var canvas = arguments[0];
# if (canvas && canvas.getContext) {
#     var ctx = canvas.getContext('2d');
#     if (ctx) {
#         console.log('Canvas context obtained');
#         ctx.font = '30px Arial';
#         ctx.fillStyle = 'black';  // Set the fill color
#         ctx.fillText('automation', 50, 50);
#         console.log('Text drawn on canvas');
#     } else {
#         console.log('Failed to get canvas context');
#     }
# } else {
#     console.log('Canvas element not found or not supported');
# }
# """

# # Execute the JavaScript to draw on the canvas
# driver.execute_script(draw_signature_script, canvas)

# canvas = driver.find_element(By.ID, 'signatureCanvas')

# JavaScript to draw the signature "automation" on the canvas
# draw_signature_script = """
# var canvas = arguments[0];
# var ctx = canvas.getContext('2d');
# ctx.font = '30px Arial';
# ctx.fillStyle = 'black';  // Set the fill color
# ctx.fillText('automation', 50, 100);
# """

# # Execute the JavaScript to draw on the canvas
# driver.execute_script(draw_signature_script, canvas)

# # Optional: Wait for a while to see the result
# time.sleep(5)
action = ActionChains(driver)
# action.move_to_element_with_offset(canvas, 50, 50).click_and_hold()
# action.move_to_element_with_offset(canvas, 50, 100).click_and_hold()
action.move_to_element_with_offset(canvas, 0, 30).click_and_hold()

# Define the movements to draw the signature "automation"
# movements = [
#     # 'a'
#     (10, 10), (0, -20), (10, 10), (10, 10), (-10, 0), (-10, 10), (0, 10), (10, 10),
#     # Space between letters
#     (20, 0),
#     # 'u'
#     (10, 10), (0, -20), (10, 0), (0, 20), (10, 0),
#     (20, 0),
#     # 't'
#     (10, -20), (0, 20), (10, -10), (-20, 0), (10, 10), (0, -20), (20, 0),
#     (20, 0),
#     # 'o'
#     (10, 10), (0, 20), (-10, 10), (-10, -10), (0, -20), (10, -10), (10, 10),
#     (20, 0),
#     # 'm'
#     (10, 20), (10, -10), (10, 10), (0, -20), (10, 0), (10, 10), (0, 20),
#     (20, 0),
#     # 'a'
#     (10, 10), (0, -20), (10, 10), (10, 10), (-10, 0), (-10, 10), (0, 10), (10, 10),
#     (20, 0),
#     # 't'
#     (10, -20), (0, 20), (10, -10), (-20, 0), (10, 10), (0, -20), (20, 0),
#     (20, 0),
#     # 'i'
#     (10, 10), (0, -20), (10, 0), (0, -10), (10, 0), (0, 20),
#     (20, 0),
#     # 'o'
#     (10, 10), (0, 20), (-10, 10), (-10, -10), (0, -20), (10, -10), (10, 10),
#     (20, 0),
#     # 'n'
#     (10, 20), (10, -10), (10, 10), (0, -20), (10, 0)
# ]

movements = [
    # 'a'
    (10, -5), (10, 10), (10, -10), (-5, -5), (-10, 0), (-5, 5), (0, 5), (5, 5), (10, -5),
    (15, 0),  # Move to the next character
    # 'u'
    (0, -5), (10, 10), (10, -10), (10, 10), (10, -10), (-10, 0), (-5, 5), (0, 5), (5, 5),
    (15, 0),  # Move to the next character
    # 't'
    (0, -10), (10, 10), (-10, 0), (0, 10), (0, -20), (20, 10),
    (15, 0),  # Move to the next character
    # # 'o'
    # (0, 5), (10, -10), (10, 10), (0, 10), (-10, 10), (-10, -10), (0, -10), (10, -10), (10, 10),
    # (15, 0),  # Move to the next character
    # # 'm'
    # (0, -10), (10, 10), (10, -10), (10, 10), (0, -10), (10, 10), (10, -10), (10, 10),
    # (15, 0),  # Move to the next character
    # # 'a'
    # (0, 5), (10, -10), (10, 10), (10, -10), (-5, -5), (-10, 0), (-5, 5), (0, 5), (5, 5), (10, -5),
    # (15, 0),  # Move to the next character
    # # 't'
    # (0, -10), (10, 10), (-10, 0), (0, 10), (0, -20), (20, 10),
    # (15, 0),  # Move to the next character
    # # 'i'
    # (0, -10), (10, 10), (-5, 0), (5, 5), (0, 5), (0, -10),
    # (15, 0),  # Move to the next character
    # # 'o'
    # (0, 5), (10, -10), (10, 10), (0, 10), (-10, 10), (-10, -10), (0, -10), (10, -10), (10, 10),
    # (15, 0),  # Move to the next character
    # # 'n'
    # (0, -10), (10, 10), (10, -10), (10, 10), (0, -10), (10, 10)
]


# Perform the drawing movements
for move in movements:
    action.move_by_offset(*move)

# Release the mouse button to complete the drawing
action.release()

# Perform the actions
action.perform()
```
