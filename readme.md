# CORS example

This example involves an index.html file attempting to load a JS script file from a 'cross' origin.  

With no alteration, this commit demonstrates scenario c.
<br>

## How to run
```
docker compose --compatibility up
```
Then visit http://localhost:8000
<br>

## Results
| Scenario | script element<br>crossorigin=anonymous attribute | Response header<br>Access-Control-Allow-Origin *<br>(sent from the cross origin) | CORS error |
| -------- | ------------------------------------------------- | ------------------------------------------------ | ---------- |
| a        | present                                           | present                                          | no         |
| b        | absent                                            | absent                                           | no         |
| c        | present                                           | absent                                           | yes        |
| d        | absent                                            | present                                          | no         |
