# jeu-de-soci-t-activit-3
#include <stdio.h>

#define NB_CASES 12

void dessiner_ligne_awale(int plateau[], int taille, int premiere_case)
{
    for(int i = 0; taille; i++)
    {
        printf("| %d ", plateau[i + premiere_case]);
    }
    printf("|\n");
}

int main() 
{
    int mains_poker[4][5];

    // Deuxième carte du premier joueur
    mains_poker[0][1] = 0;
    
    int awale[NB_CASES];
    
    for(int i=0; i<NB_CASES; i++) 
    {
        awale[i] = 4;
    }

/*  for(int i = 0; i<NB_CASES/2; i++)
    {
        printf("| %d ", awale[i]);
    }
    printf("|\n");

    for(int i = 0; i<NB_CASES/2; i++)
    {
        printf("| %d ", awale[i+6]);
    }
    printf("|\n");
    */
    dessiner_ligne_awale(awale, NB_CASES/2, 0);
    dessiner_ligne_awale(awale, NB_CASES/2, 6);
    return 0;
}