# 📘 Devoir_UVT_C

<p align="center">
  <img src="https://img.shields.io/badge/ASD-Homework-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white" />
</p>

---

## 🔵 EX1

```c
#include <stdio.h>

int main() {
    int A , B , C, A1;

    printf("give me three numbers.\n");
    scanf("%d %d %d",&A,&B,&C);
    A1=A;
    A=C;
    C=B;
    B=A1;
    printf("%d %d %d",A,B,C);
    return 0;
    
}
```

---

## 🟣 EX2

```c
#include <stdio.h>

int main() {
    int A , B , C, D;
    float E;

    printf("give me two numbers\n");
    scanf("%d %d",&A,&B);
    C=A/B;
    D=A%B;
    E=(float)A/B;
    printf("le quotient:%d\n",C);
    printf("le reste:%d\n",D);
    printf("quotient rationnel:%f\n",E);
    return 0;
    
}
```

---

## 🟢 EX3

```c
#include <stdio.h>

int main() {
    int A , B , C;

    printf("donner trois entiers:\n");
    scanf("%d %d %d", &A,&B,&C);
    if(A>=B && A>=C){
        printf("%d est le plus grand",A);
    }
    else if(B>=A && B>=C){
        printf("%d est le plus grand",B);
    }
    else{
        printf("%d est le plus ggrand",C);
    }
    return 0;
    
}
```

---

## 🟠 EX4

### 🔹 avec while:

```c
#include <stdio.h>

int main() {
    int N;
    int i = 0;
    int somme = 0;
    int produit = 1;
    float moyenne;
    int M;
    printf("donner un nombre N:");
    scanf("%d",&N);
    while(i<N){
        printf("donner un nombre:\n");
        scanf("%d",&M);
        somme=somme+M;
        produit=produit*M;
        i=i+1;
        
    }
    moyenne=(float)somme/N;
    printf("la somme est %d,le produit est %d ,la moyenne est %f",somme,produit,moyenne);
    return 0;
}
```

### 🔹 avec do ... while :

```c
#include <stdio.h>

int main() {
    int N;
    int i = 0;
    int somme = 0;
    int produit = 1;
    float moyenne;
    int M;
    printf("donner un nombre N:");
    scanf("%d",&N);
    do{
        printf("donner un nombre:\n");
        scanf("%d",&M);
        somme=somme+M;
        produit=produit*M;
        i=i+1;
        
    }while(i<N);
    moyenne=(float)somme/N;
    printf("la somme est %d,le produit est %d ,la moyenne est %f",somme,produit,moyenne);
    return 0;
}
```

### 🔹 avec for:

```c
#include <stdio.h>

int main() {
    int N;
    int somme = 0;
    int produit = 1;
    float moyenne;
    int M;
    printf("donner un nombre N:");
    scanf("%d",&N);
    for (int i=0;i<N;i++){
        printf("donner un nombre:\n");
        scanf("%d",&M);
        somme=somme+M;
        produit=produit*M;
       
    }
    moyenne=(float)somme/N;
    printf("la somme est %d,le produit est %d ,la moyenne est %f",somme,produit,moyenne);
    return 0;
}
```

> 🟡 Boucle FOR est la plus naturelle pour ce probleme

---

### 🟢 la meilleure solution avec un autre condition que N doit etre entre 1 et 15 , jai untiliser "do--while"

```c
#include <stdio.h>

int main() {
    int N;
    int somme = 0;
    int produit = 1;
    float moyenne;
    int M;
    do{
        printf("donner un nombre N:");
        scanf("%d",&N);
    }while (N < 1 || N > 15);
    for (int i=0;i<N;i++){
        printf("donner un nombre:\n");
        scanf("%d",&M);
        somme=somme+M;
        produit=produit*M;
       
    }
    moyenne=(float)somme/N;
    printf("la somme est %d,le produit est %d ,la moyenne est %f",somme,produit,moyenne);
    return 0;
}
```
