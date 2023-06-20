# rmi-example
Java RMI example. Deprecated as f****.

## Compiling and running

```
javac compute/Compute.java compute/Task.java
```

```
jar cvf classes/compute.jar compute/*.class
```

```
javac -cp ./classes/compute.jar engine/ComputeEngine.java
```

```
javac -cp ./classes/compute.jar client/ComputePi.java client/Pi.java
```

### RMI

```
set CLASSPATH=<drive>:\computeEngine
```

```
rmiregistry
```

### Server (runner)

```
java -cp <drive>:\computeEngine;<drive>:\computeEngine\classes\compute.jar -Djava.security.policy=server-win.policy engine.ComputeEngine localhost 1099
```

### Client

```
java -cp <drive>:\computeEngine;<drive>:\computeEngine\classes\compute.jar -Djava.security.policy=client-win.policy client.ComputePi localhost 1099 45
```