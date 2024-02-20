# Petsmart Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Petsmart Scraper](https://oxylabs.io/products/scraper-api/ecommerce/petsmart?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Petsmart website effortlessly. This brief guide showcases how Petsmart Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Petsmart results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Petsmart page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.petsmart.com/reptile/food/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/petsmart-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n\n\n\n\n\n\n\n\n\n<!doctype html>\n<html lang=\"en\">\n<head>\n<script src=\"https://cdn.optimizely.com/js/2373066 ... </html>",
      "created_at": "2024-02-20 12:37:10",
      "updated_at": "2024-02-20 12:37:12",
      "page": 1,
      "url": "https://www.petsmart.com/reptile/food/",
      "job_id": "7165685813794079745",
      "status_code": 200
    }
  ]
}
```
Our Petsmart Scraper empowers you to easily pull public data from any Petsmart web page. Gather crucial pet product details like pricing, customer reviews, or product descriptions, for comprehensive market analysis and competitive edge. Should you encounter any issues, don't hesitate to connect with our support team through live chat or email us at hello@oxylabs.io.