You are an expert in Selenium automation. Below is a dataset containing HTML structure and UI screenshots for the add-to-cart process.
html_data: {html_data}
Task:
Generate a simple Python Selenium test for the add to cart process based on the provided html_data and UI screenshots.
URL: `http://localhost:8080/en/`
Test scenario:

1. Open the home page.
2. Click on a product category from the top navigation menu (e.g. ART).
3. Wait for the category page to load.
4. Click on the first product in the list.
5. On the product detail page, click the "Add to cart" button.
6. Wait for the modal popup to appear after the product is added.
7. Confirm that the modal title or content includes a success message like "successfully added".
8. Optionally, locate and assert the presence of a "Proceed to checkout" button inside the modal.

`Rules:`

- Wait for the modal (popup) confirmation to appear after adding to cart.
- Confirm success by verifying the presence of the modal title that contains "successfully added" or similar.
- Do not rely on dynamic ID values — use label or section attributes like data-name instead.
- Use webdriver-manager to manage ChromeDriver.
- Use selectors strictly from html_data.
- Use WebDriverWait with a timeout of 20 seconds before interacting with elements.
- Use unittest with setUp() and tearDown().
- Before asserting any element or text, check that it exists and is not empty.
- If any required element is missing, fail the test using self.fail(...).
- Use presence_of_element_located to locate elements. Use visibility checks only when needed.
- Avoid hardcoded XPath text. Always derive selectors and conditions from html_data.
  Return only Python code using unittest.
