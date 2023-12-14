# README

Arquetipo de pruebas automatizadas usando la herramienta SerenityBDD con Screenplay

> **Soporta automatización**:
> * Web
> * Apis
> * Movil
> * As400
> * Pruebas manuales 
> * Scenarios con Karate Framework


## Herramientas y Complementos

|                                                                               **IntelliJ**                                                                                |**Java**|**Gradle**|
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------:| :----: | :----:  |
| [<img width="50" height="50" src="https://cdn.iconscout.com/icon/free/png-128/intellij-idea-569199.png">](https://www.jetbrains.com/es-es/idea/download/#section=windows) | [<img height="60" src="https://www.oracle.com/a/ocom/img/cb71-java-logo.png">](https://www.oracle.com/java/technologies/downloads/) | [<img height="50" src="https://gradle.org/images/gradle-knowledge-graph-logo.png?20170228">](https://gradle.org/releases/) |

> **NOTA**:

> * Para ejecutar el proyecto se recomienda minimo las siguientes versiones: 
>   * IntelliJ Community Edition 2021
>   * Java JDK 17
>   * Gradle 7.4
> * Una vez obtenido IntelliJ es necesario instalar los plugins de Gherkin y Cucumber for Java. (
    *[Guia de instalación plugins en intellij](https://www.jetbrains.com/help/idea/managing-plugins.html)*)

## Ejecución local

0. Clonar el proyecto

```bash
  git clone https://github.com/Jaimephyton2020/NTTData_EjercicioCalculadora
```

Para correr el proyecto de manera local se debe realizar los siguientes pasos:

1. Definir la tag de los tipos de tests que se van a ejecutar, esto lo hacemos en el archivo WebRunnerTest, para el
   ejemplo se va a correr todos los test menos los de karate, manuales y las pruebas móviles. 

```
tags = "@CalculatorJA"
```

2. Definir el driver a usarse en serenity.properties.

```
#CONFIGURACION DRIVER
webdriver.driver=chrome
```

## Comandos

El arquetipo posee 2 runners activos, uno para pruebas con SerenityBDD y otro para pruebas con Karate Framework

### Comandos SerenityBDD

Para ejecutar todos los escenarios por linea de comandos

```bash
  ./gradlew clean test --tests "com.qa.automationtest.runners.WebRunnerTest"
```
ó ejecutar dependiendo del IDE

```bash
  gradlew clean test --tests "com.qa.automationtest.runners.WebRunnerTest"
```

Para ejecutar escenarios que contengan un tag especifico

```bash
  ./gradlew clean test --tests -Dcucumber.filter.tags=@CalculatorJA" com.qa.automationtest.runners.WebRunnerTest
```
ó ejecutar dependiendo del IDE

```bash
  gradlew clean test --tests -Dcucumber.filter.tags=@CalculatorJA" com.qa.automationtest.runners.WebRunnerTest
```
