# ANNET-SUPER-HYBRIDE-V3.7-Proof
STANDARD ANNET SUPER-HYBRIDE V3.7 - Preuve de Résolution (TSP E3M.0)

## About the Project

This repository contains the implementation and validation tools for the Annet Standard, a methodology developed by Jean-Philippe Annet. This project provides an automated, secure framework for verifying computational solutions, ensuring both consistency and rigorous adherence to the established standard.

## CERTIFICATION DE RÉSULTAT

* **Algorithme :** STANDARD ANNET SUPER-HYBRIDE V3.7 (Haute Fidélité)
* **Auteur :** Jean-Philippe Annet
* **Date :** 16 Novembre 2026
* **Instance :** E3M.0 (3 162 278 Villes)
* **Type :** Traveling Salesman Problem (TSP)
* **Validité Combinatoire :** Bijection exacte certifiée (3 162 278 / 3 162 278 villes uniques)

## RÉSULTATS OFFICIELS

* **Distance Totale Exacte (Score float64) :** `1 322 425 164,64` unités (**+4,35 %** vs Record Mondial LKH-3)
* **Distance Totale Entière (TSPLIB EUC_2D) :** `1 322 397 758` unités
* **Écart vs Borne Inférieure Théorique (Held-Karp) :** **+4,95 %**
* **Pas médian / Pas moyen :** `383,55 u.` / `418,19 u.`
* **Segment maximal sur 3 162 278 pas :** `2 639,3 u.`
* **Temps de Calcul :** ~6 minutes
* **Machine :** Standard Google Colab (GPU T4 + CPU)

## VALIDATION TECHNIQUE (COMMENT VÉRIFIER LA PREUVE EN 2 SECONDES)

1. **Fichier de la solution (Tour File) :**
   Le fichier `ANNET_STANDARD_E3M_MASTER_SOLUTION.txt` joint dans ce dépôt contient la séquence ordonnée exacte des 3 162 278 identifiants de villes (`Node_ID`).

2. **Vérification d'intégrité cryptographique (SHA-256 Checksum) :**
   `9bc2e954276368ca5e34a21c79f3894a853578752f7b15a8caca72c7d60fe885`
   *(Vérifiable avec la commande : `sha256sum ANNET_STANDARD_E3M_MASTER_SOLUTION.txt`)*

3. **Audit indépendant automatisé (`verifier_preuve_zkp_annet.py`) :**
   * Téléchargez ce dépôt GitHub (`Code` -> `Download ZIP`) et décompressez-le.
   * Téléchargez le fichier des coordonnées officielles `E3M.0.csv` ici : **[Télécharger E3M.0.csv](https://drive.google.com/file/d/1uanF0EFaY5qm3miBeYeYgCoStZlJgTi-/view?usp=sharing)** et placez-le dans le même dossier.
   * Lancez le script de vérification :
     ```bash
     python verifier_preuve_zkp_annet.py
     ```
   * Le script valide en 2 secondes l'empreinte SHA-256, la visite unique des 3 162 278 villes et recalcule la distance exacte de **1 322 425 164,64 unités**.

## CONTACT & PROPRIÉTÉ

Cet algorithme et ses résultats sont la propriété intellectuelle exclusive de Jean-Philippe Annet (la licence MIT s'applique uniquement au script public de vérification, l'algorithme d'optimisation demeurant strictement confidentiel).

Pour toute demande d'audit ou collaboration : https://www.linkedin.com/in/jean-philippe-annet-514129a4
