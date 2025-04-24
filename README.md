# Analyseur-de-Texte-Python
Ce projet est un script Python conçu pour analyser le contenu textuel, qu'il provienne d'un fichier local spécifié par l'utilisateur ou d'une entrée directe via la console. L'outil fournit des statistiques clés telles que le nombre total de mots, le nombre de lignes et le nombre de caractères (en excluant les espaces et la ponctuation).

# Fonction pour lire le contenu d'un fichier
def lire_fichier(chemin_fichier):
    try:
        with open(chemin_fichier, 'r', encoding='utf-8') as fichier:
            return fichier.read()
    except FileNotFoundError:
        return None

# Fonction pour compter les mots
def compter_mots(texte):
    return len(texte.split())

# Fonction pour compter les caractères sans espaces ni ponctuation
import re
def compter_caracteres_sans_ponctuation_espaces(texte):
    return len(re.sub(r'[^a-zA-Z0-9]', '', texte))

# Logique pour l'entrée utilisateur (fichier ou ligne)
if __name__ == "__main__":
    choix = input("Analyser fichier (f) ou ligne (l) ? ").lower()
    # ... (reste du code pour la lecture et l'appel des fonctions)

Ce projet m'a permis de renforcer mes compétences en :

* Manipulation de fichiers en Python (lecture de contenu).
* Utilisation des méthodes de chaînes de caractères pour le traitement de texte (`split()`, `splitlines()`).
* Introduction et application du module d'expressions régulières (`re`) pour un filtrage précis du texte.
* Gestion de l'interaction utilisateur en ligne de commande (`input()`).
* Structuration d'un script Python pour offrir différentes options d'utilisation.

    
