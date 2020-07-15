# Proyecto Base TP2

## Prerequisitos

* Java 11 ([Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) u [OpenJDK](https://openjdk.java.net/install/))
* [Maven](https://maven.apache.org/)
* [git](https://git-scm.com/)

## Instalación

### 1. Checkout del repo

Descargar el repositorio utilizando cualquier cliente de git. Ejemplo via consola:

```shell script
git clone https://github.com/fiuba/algo3_proyecto_base_tp2.git tp2
```

El ejemplo anterior debería crear una carpeta `tp2` con los contenidos del repo.

### 2. Subir contenidos a otro repo

1. Crear un repo en github
2. Obtener el link de clonación (ej: https://github.com/mi_usuario/mi_repo_de_tp.git)
3. Ejecutar los siguientes comandos para reconfigurar el remoto:

```shell script
git remote set-url origin <link-de-clonacion>
```

Otra alternativa es:

1. Crear un repo en github
2. Obtener el link de clonación (ej: https://github.com/mi_usuario/mi_repo_de_tp.git)
3. Clonar el repositorio vacio
4. Copiar los contenidos del repositorio original al nuevo
5. Hacer commit y push

### 3. Configuración del entorno

#### 3.1 Linea de comando

Para compilar y correr la última versión de su código, simplemente ubicarse en el mismo directorio que el archivo `pom.xml` e ingresar:

```shell script
mvn clean javafx:run
```

La tarea `clean` se encarga de limpiar archivos de compilaciones anteriores. `javafx:run` compila y ejecuta la aplicación.

El output debería ser similar al siguiente:

```shell script
(base) mpicco-pc:~/code/algo3/tp2 (master) $ mvn clean javafx:run
[INFO] Scanning for projects...
[INFO] 
[INFO] ------------------------< edu.fiuba.algo3:tp2 >-------------------------
[INFO] Building tp2 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ tp2 ---
[INFO] Deleting /home/mpicco/code/algo3/tp2/target
[INFO] 
[INFO] --- javafx-maven-plugin:0.0.1:run (default-cli) @ tp2 ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /home/mpicco/code/algo3/tp2/src/main/resources
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 4 source files to /home/mpicco/code/algo3/tp2/target/classes
```

Para ejecutar las pruebas:

```shell script
(base) mpicco-pc:~/code/algo3/tp2 (master) $ mvn clean test
[INFO] Scanning for projects...
[INFO] 
[INFO] ------------------------< edu.fiuba.algo3:tp2 >-------------------------
[INFO] Building tp2 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- maven-clean-plugin:2.5:clean (default-clean) @ tp2 ---
[INFO] Deleting /home/mpicco/code/algo3/tp2/target
[INFO] 
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ tp2 ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /home/mpicco/code/algo3/tp2/src/main/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.8.0:compile (default-compile) @ tp2 ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 4 source files to /home/mpicco/code/algo3/tp2/target/classes
[INFO] 
[INFO] --- maven-resources-plugin:2.6:testResources (default-testResources) @ tp2 ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory /home/mpicco/code/algo3/tp2/src/test/resources
[INFO] 
[INFO] --- maven-compiler-plugin:3.8.0:testCompile (default-testCompile) @ tp2 ---
[INFO] Changes detected - recompiling the module!
[INFO] Compiling 1 source file to /home/mpicco/code/algo3/tp2/target/test-classes
[INFO] 
[INFO] --- maven-surefire-plugin:3.0.0-M3:test (default-test) @ tp2 ---
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running edu.fiuba.algo3.modelo.MessageTest
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.017 s - in edu.fiuba.algo3.modelo.MessageTest
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  5.495 s
[INFO] Finished at: 2020-03-09T20:25:52-03:00
[INFO] ------------------------------------------------------------------------
```

#### 3.2 IntelliJ

[Guía de configuración para IntelliJ](./IntelliJ.md)
