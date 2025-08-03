# projet-algorithmes-Analyse-d-une-phrase-

Algorithme AnalysePhrase

Variables :
    c : caractère
    longueur, nbMots, nbVoyelles : entier
    dansMot : booléen

Début
    longueur ← 0
    nbMots ← 0
    nbVoyelles ← 0
    dansMot ← Faux

    Afficher "Entrez une phrase terminée par un point : "
    Lire phrase

    Pour i ← 0 à longueur(phrase) - 1 faire
        c ← phrase[i]
        longueur ← longueur + 1

        Si c ∈ {'a','e','i','o','u','y','A','E','I','O','U','Y'} alors
            nbVoyelles ← nbVoyelles + 1
        Fin Si

        Si c = ' ' alors
            dansMot ← Faux
        Sinon Si c ≠ '.' alors
            Si dansMot = Faux alors
                nbMots ← nbMots + 1
                dansMot ← Vrai
            Fin Si
        Fin Si

        Si c = '.' alors
            Sortir de la boucle
        Fin Si
    Fin Pour

    Afficher "Longueur : ", longueur
    Afficher "Nombre de mots : ", nbMots
    Afficher "Nombre de voyelles : ", nbVoyelles
Fin

