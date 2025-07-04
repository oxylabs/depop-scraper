# Depop Scraper API

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.io/pages/gitoxy?utm_source=877&utm_medium=affiliate&groupid=877&utm_content=depop-scraper-github&transaction_id=102f49063ab94276ae8f116d224b67)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs’ [Depop Scraper](https://oxylabs.io/products/scraper-api/ecommerce/depop?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Depop website effortlessly. This brief guide explains how an Depop Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Depop results by providing your own URLs to our service. We can return the HTML for any Depop page you like.

#### Python code example

The example below illustrates how you can get HTML of Depop page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.depop.com/category/womens/bottoms/?categorypath=womens&categorypath=bottoms'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/depop-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"us\"><head><meta charSet=\"utf-8\"/><meta name=\"viewport\" content=\"width=dev ... </html>",
      "created_at": "2023-12-18 10:26:59",
      "updated_at": "2023-12-18 10:27:03",
      "page": 1,
      "url": "https://www.depop.com/category/womens/bottoms/?categorypath=womens&categorypath=bottoms",
      "job_id": "7142460232361325569",
      "status_code": 200
    }
  ]
}
```
With our Depop Scraper, you can smoothly gather all public data from any Depop webpage. Acquire the critical product details, including photographs, seller histories, or shipping details, thereby providing an essential foundation for your market analysis and outperforming your business rivals. If you need assistance, reach out to our support team through live chat or drop us an email at hello@oxylabs.io.
