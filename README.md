This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

# similarity-api

### About:

This is an educational project. This is an API service that helps to compare two texts by their identity.

**Frontend** is fully responsive for all devices, **TailwindCSS** is also used as a styling approach

## How to use:

### Nodejs - 
```node
const axios = require("axios");

const options = {
    method: 'POST',
    url: 'https://similarity-api-dgce.vercel.app/api/v1/similarity',
    params: {
      text1: 'First text',
      text2: 'Second text'
    },
    headers: {
      'Authorization': 'YOUR_API_KEY',
    }
  };
  
axios.request(options).then(function (response) {
    console.log(response.data);
}).catch(function (error) {
    console.error(error);
});
```

#

### Python -

```python
import requests

url = 'https://similarity-api-dgce.vercel.app/api/v1/similarity'
api_key = 'YOUR_API_KEY'
text1 = 'First text'
text2 = 'Second text'

headers = {
    'Authorization': api_key
}

payload = {
    'text1': text1,
    'text2': text2
}

response = requests.post(url, headers=headers, json=payload)

if response.status_code == 200:
    data = response.json()
    print(data)
else:
    print(f'Request failed with status code {response.status_code}')

```


#

![Preview](https://i.ibb.co/gFXwbgD/2023-04-21-16-42-41.png)
![Preview](https://i.ibb.co/GsJyHdP/2023-04-21-16-42-53.png)

To Visit App:

Deployed in **Vercel** - `https://similarity-api-dgce.vercel.app/documentation`

