
-get legacy address from bit core testnet from cli
 > getnewaddress "test" legacy

1) Request: http://localhost:8000/block/0
```
{
    "hash": "82507003279afee07c482d01013e342672672849f356b17587b8c125d3e8c829",
    "height": 0,
    "body": "7b2264617461223a2247656e6573697320426c6f636b227d",
    "time": "1652631255",
    "previousBlockHash": null
}
````
![](https://github.com/VimalKumarS/udacity_blockchain_project_1/blob/main/Screen%20Shot%202022-05-14%20at%206.58.32%20PM.png)
2) Request: http://localhost:8000/requestValidation
{
    "address":"mq8ULMhPDE1565YjCFaVo81vz5pEfEXnbp"
}
```
"mq8ULMhPDE1565YjCFaVo81vz5pEfEXnbp:1652632388:starRegistry"
```
![](https://github.com/VimalKumarS/udacity_blockchain_project_1/blob/main/Screen%20Shot%202022-05-14%20at%207.18.00%20PM.png)

3) Sign message
"IED6V+ddOJ0zL6qFxDy5XvtKS9y1Wi1Pp18CjeklC9H9FY1x7knBk/7yKz8wZIexSc6IIfYvoJsUWCqHJAqUJck="

4) Request: http://localhost:8000/submitstar
```
payload 
{
    "address":"mq8ULMhPDE1565YjCFaVo81vz5pEfEXnbp",
    "signature":"IED6V+ddOJ0zL6qFxDy5XvtKS9y1Wi1Pp18CjeklC9H9FY1x7knBk/7yKz8wZIexSc6IIfYvoJsUWCqHJAqUJck=",
    "message":"mq8ULMhPDE1565YjCFaVo81vz5pEfEXnbp:1652632388:starRegistry",
         "star": {
         "dec": "68° 52' 56.9",
         "ra": "16h 29m 1.0s",
         "story": "Testing the story 4"
     }
}
```
![](https://github.com/VimalKumarS/udacity_blockchain_project_1/blob/main/Screen%20Shot%202022-05-15%20at%209.34.21%20AM.png)

5) Request: http://localhost:8000/blocks/mq8ULMhPDE1565YjCFaVo81vz5pEfEXnbp