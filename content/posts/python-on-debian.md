---
title: "Python on Debian"
date: 2023-02-17T14:26:05-07:00
tags: []
draft: true
---
```sudo apt update && sudo apt upgrade```

```sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev```

```wget https://www.python.org/ftp/python/3.10.0/Python-3.10.0.tgz```

```tar -xf Python-3.10.*.tgz```

```cd Python-3.10.*/
./configure --enable-optimizations```

```make -j 4```

```sudo make altinstall```


```sudo ln -s /usr/local/bin/python3.11 /usr/local/bin/python```

```sudo apt install python3-pip```


[source](wget https://www.python.org/ftp/python/3.10.0/Python-3.10.0.tgz)
