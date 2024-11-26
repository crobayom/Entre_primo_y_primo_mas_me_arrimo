# Numeros-primos

###### Estaba pensando en ponerle de titulo al repositorio: Entre primo y primo mas me arrimo, pero no me dio el coraje

#### En este repositorio se comentara todo el desarrollo de la actividad necesaria para completar el reto 3

---
### Requisitos

[] Escribir en pseudocodigo un algoritmo que permita encontrar todos los numeros primos hasta un numero n

[] Hacer un diagrama de flujo que permita encontrar todos los numeros primos hasta un numero n

---

### Pseudocodigo: 

```
n:entero
i:entero
d:entero
Inicio
i:=2
d:=0
si n==1
//no hay primos que encontrar;
si n==2
//solo esta 2 como primo
Escribir ("2");
Para (m<-2;m<=n;m++){
Para (i<-2;i<√(n)+1;i++){
Si modulo (m,i) !=0
d:=d+1;
}
si d==0
//El actual n es primo
escribir ("n, ");+
d:=0
}
```

### Diagrama de flujo:

```mermaid
graph TD;
1(Incio) --> 2[numero n];
2[numero n] --> 3[numero d=0];
3[numero d=0] --> 4[numero e=1];
4[numero e=1] --> 5["Lista de numeros desde 2 hasta (n**0.5)+1"];
5["Lista de numeros desde 2 hasta (n**0.5)+1"] --> 6[i=2];
6[i=2] --> 7{"¿ El numero e actual es 1 ?"};
7{"¿ El numero e actual es 1 ?"} --- sí --> 12[d=d+1];
7{"¿ El numero e actual es 1 ?"} --- no --> 9{"¿ El numero e actual es 2 ?"};
9{"¿ El numero e actual es 2 ?"} --- si --> 16{"¿ d es 0 ?"}
9{"¿ El numero e actual es 2 ?"} --> a[no] --> 11{"¿El residuo de e/i es 0?"};
11{"¿El residuo de e/i es 0?"} --> b[si] --> 12[d=d+1];
11{"¿El residuo de e/i es 0?"} --> c[no] --> 13[i=i+1];
13[i=i+1] --> 14{"¿ i es menor que (n**0.5)+1 ?"};
14{"¿ i es menor que (n**0.5)+1 ?"} --> d[si] --> 11{"¿El residuo de e/i es 0?"};
14{"¿ i es menor que (n**0.5)+1 ?"} --> e[no] --> 16{"¿ d es 0 ?"};
12[d=d+1] --> 16{"¿ d es 0 ?"};
16{"¿ d es 0 ?"} --> f[si] --> 10[El numero e actual es un numero primo];
16{"¿ d es 0 ?"} --> g[no] --> 17[El numero e actual no es un numero primo];
10[El numero e actual es un numero primo] --> 15["Escribir (e) Escribir (, )"];
15["Escribir (e) Escribir (  )"] --> 18[d=0];
17[El numero e actual no es un numero primo] --> 18[d=0];
18[d=0] --> 18a[i=2];
18a[i=2] --> 19[e=e+1];
19[e=e+1] --> 20{"¿ e es menor o igual que n ?"};
20{"¿ e es menor o igual que n ?"} --> h[si] --> 9{"¿ El numero e actual es 2 ?"};
20{"¿ e es menor o igual que n ?"} --> i[no] --> 21(Fin);

```
