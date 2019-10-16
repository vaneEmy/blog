## Personal Blg

- clone the project

```
git clone https://github.com/vaneEmy/blog
```

- Initialize git submodules

```
git submodule init 
```

- Update submodules

```
git submodule update 
```
**Note:** Public and hugo-universal-theme must be empty directories.


- Deploy in local host

```
git server -w
```

## Deploy

- Delete content from public directory:

```
cd public/

rm -rf *
```

- Generate public content

```
cd ../

hugo
```

- Publish public/



```
cd public/
git status
git push origin master
```





