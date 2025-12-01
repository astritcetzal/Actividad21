# 🛡️ Implementación del Algoritmo de Cifrado Hill

Este trabajo contiene una implementacion funcional del **Cifrado Hill**, un algoritmo de cifrado por bloques que utiliza algebra lineal para transformar texto en texto cifrado y viceversa. Este repositorio esta diseñado con el fin de demostrar la comprension del algoritmo de criptografico y a su vez aplicando tecnologias como HTML, Java Script y CSS.

## 👨‍💻 Información del Estudiante

- **Nombre:** Astrit Airan Cetzal
- **Matrícula:** SW2509028
- **Grupo:** C
- **Materia:** Fundamentos de álgebra
- **Cuatrimestre:** Primer Cuatrimestre
- **Carrera:** TSU en Desarrollo e Innovación de Software
- **Profesor:** Jorge Javier Pedrozo Romero

---

## 📋 1. Implementacion del Cifrado Hill
El cifrado Hill sustituye bloques de *m* letras por otros *m* bloques del mismo, utilizando una matriz invertible de *m x m* sobre el alfabeto (modulo 26).

### Funcionalida principal en esta actividad
**1. Encriptacion (Cifrado)**: Transforma un mensaje de texto plano en un mensaje cifrado, utilizando una matriz clave de 2 x 2.
**2. Desencriptacion (Cifrado)**:Calcula la matriz inversa modular de la clave original y la utiliza para revertir el texto cifrado a su estado original de texto. 

---

## 2. Fundamento Matemático

### - Alfabeto y el módulo
- Se utiliza el afabeto en español contando solo 26 letras.
- Cada letra se mapea a un número de 0 a 25.
- Todas las operaciones se realizan módulo 26 por el tamaño del alfabeto.

### - Manejo de la clave (matriz *K*)
La matriz K de m x m es la clave de su funcionamiento. Para que la clave sea válida y el mensaje se pueda desencriptar, el determinante de la matriz no debe ser 0 y debe ser coprimo con el modulo ( en este caso 26). Es decir mcd(det(K),26)=1. Lo cual asegura que el determinante tenga un inverso multiplicativo módulo 26.

### - Encriptacion
El cifrado se realiza multiplicando los vectores numéricos del texto plano(P) por la matriz clave (K), y tomando el resultado del módulo 26.

```
C= (K * P) (mod 26)

```
Donde *C* es el vector numerico del texto cifrado.

### - Desencriptacion (matriz inversa)
La desencriptación require el uso de la matriz inversa modular de la clave, denotada como K^-1.
```
P= (K^-1 * C) (mod 26)

```  
La matriz inversa se calcula mediante la formula: 

```
K^-1 = det (K)^-1 * Adjunta(K) (mod 26)
```
Donde $\det(K)^{-1}$ es el inverso multiplicativo del determinante módulo 26. Este inverso existe si y solo si $\text{mcd}(\det(K), 26) = 1$.

- Implementación en JavaScript: El código incluye funciones para calcular el determinante, encontrar el inverso modular del determinante etc.

---
## 3. Instruciones de uso

1. Ingreso de Mensaje: Escribe el mensaje que deseas cifrar.

2. Operación: Presiona el botón "Encriptar" que se encuentra en la parte inferior despues para descifrar debes irte al boton "Desencriptar" que se encuentra en la parte supeior y luego presionar "Desencriptar" que se encuentra en la parte inferior izquierda.

3. Validación de Clave: El sistema validará automáticamente si el determinante de la matriz clave es coprimo con 26. Si no lo es, mostrará un mensaje de error indicando que la clave no es invertible.

### 4. Personalización y diseño

- Esquema de Colores: Se utiliza una paleta de colores moderna
- Tipografía: Se emplea una fuente clara y monoespaciada para el texto cifrado y los números de la matriz, mejorando la legibilidad.
- Validación Visual: Los mensajes de error y los resultados (texto cifrado/descifrado) se presentan en cajas de alerta claras y con códigos de color para una retroalimentación inmediata.
---


## 🚀 Instalación y Uso

### Prerrequisitos
- Node.js (versión 14 o superior)
- Git

### Clonar el repositorio
```bash
git clone https://github.com/TU-USUARIO/fundamentos-programacion-practica-1.git
cd fundamentos-programacion-practica-1
```

### Instalar dependencias
```bash
npm install
```

### Ejecutar tests
```bash
npm test
```

### Ejecutar tests en modo watch
```bash
npm run test:watch
```

### Ver cobertura de código
```bash
npm run test:coverage
```

---

## 📁 Estructura del Proyecto

```
Algebra_final/
│
├── index.html         # ⭐ Página
├── RAEADME.md     
├── script.js          # Configuración del proyecto
|__ style.scc          # Estilo de la página

```

---

## 💡 Aprendizajes Clave

### Lo que más me costó
- **Java script**: Hacer la funcion para desencriptar
- **HTML**:Poner el boton para desencriptar.


### Lo que más me gustó
- **CSS**: Ponerle estilo a la página 

---

## 📚 Recursos Utilizados

- [MDN Web Docs - JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript)
- [JavaScript.info](https://es.javascript.info/)
- [Stack Overflow](https://stackoverflow.com)


---


## 📝 Historial de Commits

```bash
# Ver mi historial completo
git log --oneline --graph --decorate
```

---

## 🤝 Agradecimientos

- **Profesor Jorge Javier Pedrozo Romero** por la estructura del curso y la práctica
- **Tecnológico de Software** por la formación integral

---

## 📧 Contacto

- **Email Institucional:** astrit.cetzal@tecdesoftware.edu.mx
- **GitHub:** [@astritcetzal](https://github.com/astritcetzal)

---

## 📄 Licencia

Este proyecto es parte de las actividades académicas del **Tecnológico de Software** y está bajo la licencia MIT.

---

<div align="center">

**⭐ Si te gustó este proyecto, dale una estrella ⭐**

Hecho con 💙 por Astrit Airan Cetzal Cetzal - 2025

</div>