You are an `expert` in Selenium automation.
Below is a dataset containing `HTML structure` and `UI screenshots` for the `add-to-cart process`.
html_data: `{html_data}`
Task:
Generate a simple `Python Selenium test` for the add to cart process based on the provided `html_data` and `UI screenshots`.
`URL: http://localhost/`
\_Test scenario:\*

1. Open the `home page`.
2. Hover over the first product.
3. Click the revealed `"Add to cart"` button.
4. Click the cart icon to open the`popup cart`.
5. Wait for the `popup` to become visible.
6. Click `"View cart"` or similar button inside the popup.
7. On the cart page, verify that the product appears in the `cart list`.

_Rules:_

- Hover over a product item to reveal the `"Add to cart" button`.
- Open the cart popup by clicking the `cart icon`.
- Confirm success by checking that the popup contains at least one item.
- Use `webdriver-manager` to manage ChromeDriver.
- Use selectors strictly from `html_data`.
- Use `WebDriverWait` with a timeout of 20 seconds before interacting with elements.
- Use unittest with `setUp()` and `tearDown()`.
- Before asserting any element or text, check that it exists and is not empty.
- If any required element is missing, fail the test using `self.fail(...)`.
- Avoid hardcoded `XPath` text. Always derive selectors and conditions from `html_data`.
- Return only `Python code` using `unittest`.
