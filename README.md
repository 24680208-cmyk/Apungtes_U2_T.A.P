# 📚 Unidad 2: Componentes y Librerías

## 📌 Introducción

En el desarrollo de software moderno, la organización del código es un aspecto fundamental para garantizar aplicaciones eficientes, escalables y fáciles de mantener. A medida que los sistemas crecen en complejidad, se vuelve necesario dividirlos en partes más pequeñas, reutilizables y bien estructuradas.

Para lograr esto, se utilizan componentes, librerías y paquetes, los cuales permiten construir sistemas modulares, mejorar la legibilidad del código y facilitar el trabajo en equipo.

En esta unidad se estudian estos conceptos desde un enfoque teórico y práctico, incluyendo múltiples ejemplos en diferentes lenguajes de programación.

---

## 🔹 2.1 Definición conceptual de componentes, paquetes y librerías

### 🧩 Componentes

Un componente es una unidad modular de software que encapsula una funcionalidad específica y puede reutilizarse en diferentes partes de un sistema.

---

### ✔️ Tipos de componentes

#### 🔸 Componentes visuales
- Botones  
- Ventanas  
- Formularios  
- Menús  
- Tablas  

#### 🔸 Componentes no visuales
- Clases de lógica  
- Validaciones  
- Procesamiento de datos  
- Algoritmos  

---

### 🔧 Características

- Encapsulamiento  
- Reutilización  
- Modularidad  
- Independencia  
- Escalabilidad  

---

### 📦 Librerías

Una librería es un conjunto de funciones o clases reutilizables.

---

### 🗂️ Paquetes

Un paquete organiza módulos dentro de un proyecto.

---

## 🔹 2.2 Uso de librerías proporcionadas por el lenguaje

Las librerías permiten ahorrar tiempo y mejorar la calidad del código.

---

### 🐍 Python - math

```python
import math

print(math.sqrt(25))
print(math.pow(2,3))
print(math.factorial(4))
```

###  Python - random

```python
import random

print(random.randint(1,100))
print(random.choice(["rojo","azul","verde"]))
```

###  Python - statistics

```python
import statistics

datos = [10,20,30,40]

print(statistics.mean(datos))
```
### Java - Scanner
```Java
import java.util.Scanner;

public class Entrada {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.println("Ingresa un número:");
        int n = sc.nextInt();
        System.out.println("Número:", n);
    }
}
```
### Java - Math
```Java
public class Matematicas {
    public static void main(String[] args){
        System.out.println(Math.sqrt(25));
        System.out.println(Math.pow(2,3));
    }
}
```
### JavaScript - Array
```JavaScript
const numeros = [1,2,3];

const dobles = numeros.map(n => n*2);

console.log(dobles);
```

### 2.3 Creación de componentes
🔸 Componente no visual (Calculadora)
```python
class Calculadora:

    def suma(self,a,b):
        return a+b

    def resta(self,a,b):
        return a-b

    def multiplicacion(self,a,b):
        return a*b

    def division(self,a,b):
        if b!=0:
            return a/b
        return "Error"

calc = Calculadora()

print(calc.suma(5,2))
```

### Componente extra (Conversor)
```python
class Conversor:

    def celsius_fahrenheit(self,c):
        return (c*9/5)+32

conv = Conversor()

print(conv.celsius_fahrenheit(30))
```
### Componente validación
```python
class Validador:

    def es_par(self,n):
        return n%2==0

    def es_primo(self,n):
        for i in range(2,n):
            if n%i==0:
                return False
        return True

v = Validador()

print(v.es_primo(7))
```

### Componente visual (Java)
```Java
import javax.swing.*;

public class Ventana {
    public static void main(String[] args){

        JFrame v = new JFrame("App");
        JButton b = new JButton("Aceptar");

        v.add(b);
        v.setSize(300,200);
        v.setVisible(true);
    }
}
```
### 2.4 Creación de librerías propias
### Estructura
mi_libreria/

 ├── operaciones.py
 
 └── main.py

 ### operaciones.py
 ```python
def suma(a,b):
    return a+b

def resta(a,b):
    return a-b

def multiplicacion(a,b):
    return a*b
```
### main.py
 ```python
import operaciones

print(operaciones.suma(5,3))
```

### Ejemplo avanzado (Python)
 ```python
def es_par(n):
    return n%2==0

def cuadrado(n):
    return n*n
```

### Java paquete
```Java
package utilidades;

public class Operaciones {

    public int suma(int a,int b){
        return a+b;
    }

    public int resta(int a,int b){
        return a-b;
    }
}
```

### Uso
```Java
import utilidades.Operaciones;

public class Main {

    public static void main(String[] args){

        Operaciones op = new Operaciones();

        System.out.println(op.suma(3,4));
    }
}
```
## 🧠 Conclusión

En el desarrollo de esta unidad se logró comprender la importancia de los componentes, las librerías y los paquetes como elementos fundamentales en la construcción de software moderno. Estos conceptos no solo permiten organizar mejor el código, sino que también facilitan la reutilización de funcionalidades, lo que reduce significativamente el tiempo de desarrollo y la probabilidad de errores.

Los componentes, tanto visuales como no visuales, representan una forma eficiente de dividir un sistema en partes más pequeñas e independientes. Esto permite que cada parte cumpla una función específica dentro del sistema, favoreciendo la modularidad y haciendo que el software sea más fácil de entender, mantener y escalar. Además, la separación entre la lógica y la interfaz contribuye a una mejor estructura del proyecto.

Por otro lado, el uso de librerías proporcionadas por los lenguajes de programación demuestra cómo es posible aprovechar herramientas ya desarrolladas y optimizadas. Esto no solo agiliza el proceso de desarrollo, sino que también garantiza el uso de soluciones probadas, aumentando la confiabilidad del software. A través de los ejemplos realizados, se observó cómo estas librerías permiten resolver problemas complejos con pocas líneas de código.

Asimismo, la creación de componentes propios permite adaptar el software a necesidades específicas, lo que resulta fundamental en proyectos reales. El desarrollo de clases, funciones y módulos personalizados favorece la reutilización del código dentro del mismo proyecto o incluso en otros, lo que mejora la productividad del desarrollador.

En cuanto a la creación de paquetes y librerías definidas por el usuario, se destaca su importancia para organizar proyectos de mayor tamaño. Una buena estructura de carpetas y módulos facilita la navegación dentro del código, permite el trabajo colaborativo y hace que el sistema sea más escalable. Además, el uso de buenas prácticas, como la correcta nomenclatura y documentación, contribuye a la calidad del software.

En conclusión, el uso adecuado de componentes, librerías y paquetes es esencial para el desarrollo de aplicaciones modernas. Estos elementos permiten construir sistemas más ordenados, reutilizables y eficientes, facilitando su mantenimiento y evolución a lo largo del tiempo. Su correcta aplicación no solo mejora la calidad del software, sino que también fortalece las habilidades del desarrollador en la creación de soluciones más profesionales y estructuradas.
