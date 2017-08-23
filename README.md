# Welcome to Flatte

Client-Side nosql Firebase Realtime Database save management. 

## Demo
[Flatte Manifesto Builder](https://flatte.maxabab.com)

## Example
#### Javascript Code
```javascript
flatte.do([
  Ref:"customer",
  data:{"-KrvGZuVwqwerty":{"firsName":"Elon","lastName": "Musk","twitter": "@elonmusk"}}
]);
```

#### Manifesto Json
```json
{
     "customer": {
          "childs": {
               "customerID": {
                    "_q": {"ID": true}
	}}},
     "employe": {
          "childs": {
               "employeID": {
					"_q": {"ID": true},
	                "childs": {
						"firstName": {
							"_q": {
								"saveValue": {"filter": "uppercase"},
								"deleteValue": ".auth",
								"copy":[{"saveValue": "$","deleteValue": "null","path": "/contact/#employeID/firstName"}]
}}}}}}}
					
```

## License
- Flatte is licensed under the MIT license.
  - [http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT)
