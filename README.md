# Numeros-primos

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
7{"¿ El numero e actual es 1 ?"} --- sí --> 8[El numero n actual no es un numero primo];
7{"¿ El numero e actual es 1 ?"} --- no --> 9{"¿ El numero e actual es 2 ?"};
9{"¿ El numero e actual es 2 ?"} --- si --> 10[El numero n actual es un numero primo];
9{"¿ El numero n actual es 2 ?"} --- no --> 12{"¿ El residuo de n/i es 0 ?"};
12{"¿ El residuo de n/i es 0 ?"} --- si --> 13[El numero i es divisor del numero n actual, por tanto n no es primo];
10[El numero n actual es un numero primo] --> 11["Escribir (n) Escribir (', ')"];
```
