To test the session affinity through manual curl request, follow below steps:

steps1: ```curl -kv cookie.ca/```

Identify the JESSIONID and GCLB cookie values from the output and use them in the curl request as below:

step2: ```curl -b "JESSIONID=69450872-c163-4765-a52c-199ab82c279e; GCLB=CNmRua_5k-TAcw" -kv cookie.ca/```

To continuously send the requets, use while loop:
```while true; do curl -ks -b "JESSIONID=69450872-c163-4765-a52c-199ab82c279e; GCLB=CNmRua_5k-TAcw" -kv cookie.ca/; done ```
