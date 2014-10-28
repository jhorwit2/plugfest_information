Information about PlugFest
====================


### Lets get some data!

The data that ThreatStop is providing us will be in JSON format that can be retrieved from a public url. Here is a quick few examples about how you could retrieve this information:

**Python**
```python
import requests

response = requests.get('http://www.joshuahorwitz.me/test.json')

data = response.json()
print data
```

**NodeJS**
```javascript
var request = require('request')

var url = 'http://joshuahorwitz.me/test.json';

request({
    url: url,
    json: true
}, function (error, response, body) {
    console.log(body);
});
```

**Ruby**
```ruby
response = Net::HTTP.get_response("www.joshuahorwitz.me","/test.json")
puts response.body
```

### How can I use this data?!

Well, here would be my process flow if I was doing this project.

1. I'd use a script to retrieve the data on a timer every N minutes.
2. Process the data in some way and save it to the database
3. Have the client request the data and retrieve it from the database
4. Rinse and Repeat

So how could you do this? Glad you asked.

**Lets start with the script to retrieve data**

