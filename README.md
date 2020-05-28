# LR1110-Node-Red
Example of Node-Red flow that communicates with Lora Cloud Server

## Instructions for use

1. Open Node-RED dashboard
2. Click three horizontal bars (hamburger icon)  in top right corner of dashboard.
3. Select import option and copy contents of lr1110_flow.json into window or just import json file.
4. You will see new tab named **LR1110 example** above dashboard. Click it to see flow that you just imported.


## Explanation of example

Example shows how to build a body of post request and how to send it Lora Cloud server.
After deploying the flow, we can click inject node to send the request to the server and observe response in debug window.
**Important:** this example will not work out of the box, user needs to provide AUTH_TOKEN inside of *Prepare request* node. Token is provided by Lora Cloud on this [link](https://www.loracloud.com/), after creating a free profile. Maximum use of tokens is limited to 1000 per month for free subscription.

## Example of a good response:

If request was successfully resolved, then returned response will look something like this:

```javascript
{
  "result": {
    "accuracy": 4.0,
    "capture_time_gps": 1271763033.13784,
    "capture_time_utc": 1587727815.13784,
    "ecef": [
      4230992.66,
      1186203.17,
      4608044.5
    ],
    "gdop": 4.1,
    "llh": [
      46.5534,
      15.6614,
      385.5
    ]
  },
  "warnings": []
}
```
