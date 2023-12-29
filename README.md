# getjsontable

JS library which helps to get some site table converted to json

``⚠️ NOTE: this library may work unstable, so please create an issue if you encounter an error``

## Installation

with **NPM**
```
npm install getjsontable
```

with **YARN**
```
yarn add getjsontable
```

## Code example
```javascript
import table from "getjsontable";
table("https://sa-mp.ru/adminhistory-aurum", "post", undefined, {
  hideColumnsDescription: true,
})
  .then((res) => console.log(res[0]))
  .catch((err) => {
    console.log(err);
    console.log(`this is an error`);
  });
```
| Option  |  Type |
|---|---|
| url  | ``string``  |
| method  | ``string``  |
| axiosOptions (options of http request)  | ``AxiosRequestConfig<any,any>`` [(docs reference)](https://axios-http.com/docs/req_config)  |
| options | ``IOptions`` 
## ``IOptions`` type
| Option | Explanation |
| ---- | ----|
| ``hidehideColumnsDescription`` (boolean) | Hide the columns explanation

# Result
```
[
  {'0': <first column data of first row>, '1': <second column data of first row>, .... }
]
```
