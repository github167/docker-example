Reference links:

https://github.com/jessfraz/dockerfiles

https://github.com/forwardcomputers/dockerfiles

Using nodejs
```
alias node="docker run -it --user $(id -u):$(id -g) --rm -v ~/myapp:/usr/src/app -w /usr/src/app node"
alias npm="docker run -it --user $(id -u):$(id -g) --rm -v ~/myapp:/usr/src/app -w /usr/src/app node npm"
alias npx="docker run -it --user $(id -u):$(id -g) --rm -v ~/myapp:/usr/src/app -w /usr/src/app node npx"

# cd ~/myapp; node index.js
# npm init -y
# npx http-server
# node /bin/bash

```



