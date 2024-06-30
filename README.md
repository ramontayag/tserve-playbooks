Start by installing openssh in the server and connecting to it.

```
ssh username@ip.com
```

The rest can be done remotely. In the server:


```
sudo apt-get clean && \
sudo apt-get upgrade && \
sudo apt-get update -yqq && \
  sudo apt-get install ansible-core
```
