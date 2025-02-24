
# SNKRS Redirect

This repository contains a simple HTML page that redirects users to the SNKRS app for a specific product.  It uses a URL parameter `sku` to identify the product.

## How it works

The HTML file uses JavaScript to:

1. Extract the `sku` value from the URL's query parameters.
2. Construct a SNKRS app link in the format `snkrs://product/{sku}`.
3. Redirect the user to this constructed link.  This will attempt to open the SNKRS app if it's installed.

## Usage

To use this redirect, you need to provide the product's SKU as a query parameter in the URL. For example:

    https://your-redirect-domain.com/redirect.html?sku=YOUR_PRODUCT_SKU

Replace `YOUR_PRODUCT_SKU` with the actual SKU of the product you want to link to. You'll also need to host the `redirect.html` file on a web server (replace `your-redirect-domain.com` with your domain or hosting URL). ## Example Let's say the product SKU is `12345`. The URL would be:

    https://your-redirect-domain.com/redirect.html?sku=12345

When a user visits this URL, they will be redirected to the SNKRS app page for product `12345` (if the app is installed). #
## Important Considerations 
**SNKRS App Availability:** This redirect relies on the user having the SNKRS app installed. If the app is not installed, the redirect will likely fail and the user may see an error or be taken to a default browser page. There is no fallback provided in this code.
**Hosting:** You will need to host the `redirect.html` file on a web server to make it accessible via a URL. 
**Mobile Devices:** This redirect is primarily intended for use on mobile devices where the SNKRS app can be opened.


## License

This project is licensed under the MIT License with a Non-Production Clause. This means you are free to use, modify, and distribute the code for non-commercial purposes, but it cannot be used in a production environment. See the [LICENSE](LICENSE) file for the full license text.
