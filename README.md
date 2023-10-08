# tp1


Qst1

#include <stdio.h>
#include <stdlib.h>

int main() {
char nom[100];

printf("Veuillez entrer votre nom : ");
scanf("%s", nom);
printf("Bienvenue, %s !\n", nom);

return 0;

Qst2

#include <stdio.h>
#include <stdlib.h>

int main() {
int nombre;
printf("Veuillez entrer un nombre : ");
scanf("%d", &nombre);
if (nombre % 2 == 0) {
printf("%d est un nombre pair.\n", nombre);
} else {
printf("%d est un nombre impair.\n", nombre);
}
}

Qst3
#include <stdio.h>
#include <stdlib.h>

int main() {
int nombre;

printf("Veuillez entrer un nombre : ");
scanf("%d", &nombre);


if (nombre % 2 == 0) {
    printf("%d est un nombre pair.\n", nombre);
} else {
    printf("%d est un nombre impair.\n", nombre);
}

}

Qst4
#include <stdio.h>
#include <stdlib.h>

int main() {
int i;

for (i = 1; i <= 10; i++) {
    printf("%d\n", i);
}

return 0;

}

Qst5

#include <stdio.h>
#include <stdlib.h>

int main() {

int tableau[5] = {10, 20, 30, 40, 50};


printf("Les valeurs du tableau sont : ");
for (int i = 0; i < 5; i++) {
    printf("%d ", tableau[i]);
}
printf("\n");

return 0;

}

Qst7

#include <stdio.h>
#include <stdlib.h>

int main() {

int tableau[] = {10, 5, 20, 25, 15};
int taille = sizeof(tableau)/sizeof(tableau[0]);

int plusGrand = tableau[0];


for (int i = 1; i < taille; i++) {
    if (tableau[i] > plusGrand) {
        plusGrand = tableau[i];
    }
}


printf("Le plus grand nombre dans le tableau est : %d\n", plusGrand);

return 0;

}

Qst10
#include <stdio.h>

int sommeElements(int tableau[], int taille) {
int somme = 0;
for (int i = 0; i < taille; i++) {
somme += tableau[i];
}
return somme;
}

int main() {
int monTableau[] = {1, 2, 3, 4, 5};
int taille = sizeof(monTableau) / sizeof(monTableau[0]);

int resultat = sommeElements(monTableau, taille);
printf("La somme des éléments du tableau est : %d\n", resultat);

return 0;

}

Qst11

#include <stdio.h>

int main() {
int numeroJour;

printf("Entrez un nombre entre 1 et 7 : ");
scanf("%d", &numeroJour);

switch (numeroJour) {
    case 1:
        printf("Lundi\n");
        break;
    case 2:
        printf("Mardi\n");
        break;
    case 3:
        printf("Mercredi\n");
        break;
    case 4:
        printf("Jeudi\n");
        break;
    case 5:
        printf("Vendredi\n");
        break;
    case 6:
        printf("Samedi\n");
        break;
    case 7:
        printf("Dimanche\n");
        break;
    default:
        printf("Le numéro saisi n'est pas valide. Veuillez entrer un nombre entre 1 et 7.\n");
        break;
}

return 0;

}

Qst12

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {

srand(time(0));


int nombreSecret = rand() % 100 + 1;

int nombreDevine;
int essais = 0;
int limiteEssais = 10; 

printf("Bienvenue dans le jeu de devinette !\n");
printf("Devinez un nombre entre 1 et 100.\n");

while (1) {
    printf("Entrez votre devinette : ");
    scanf("%d", &nombreDevine);
    essais++;

    if (nombreDevine < nombreSecret) {
        printf("Trop bas. Essayez encore.\n");
    } else if (nombreDevine > nombreSecret) {
        printf("Trop haut. Essayez encore.\n");
    } else {
        printf("Bravo ! Vous avez deviné le nombre secret %d en %d essais.\n", nombreSecret, essais);
        break; 
    }

    if (essais >= limiteEssais) {
        printf("Désolé, vous avez atteint le nombre maximal d'essais. Le nombre secret était %d.\n", nombreSecret);
        break;
    }
}

return 0;

}

