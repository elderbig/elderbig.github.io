## 南北朝
```plantuml
@startuml
[*] --> 开始
开始-->结束
@enduml
```

## install graphviz on linux from source



* download source from gitlab

```
wget https://gitlab.com/api/v4/projects/4207231/packages/generic/graphviz-releases/2.49.1/graphviz-2.49.1.tar.gz
```

* build graphviz from source

```
./configure --prefix=/home/test/graphviz
make
make install
```



* use graphviz on in plantuml

```
export PATH=/home/test/graphviz/bin:$PATH
java -jar plantuml.jar -testdot #test if graphviz can be use
java -jar plantuml.jar -picoweb
```

