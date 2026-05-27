# Importation des bibliothèques
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Création des données
mois = ["Janvier", "Février", "Mars", "Avril", "Mai", "Juin"]
ventes = [1500, 1800, 1700, 2000, 2200, 2500]

# Création du DataFrame
df = pd.DataFrame({
    "Mois": mois,
    "Ventes": ventes
})

# Affichage du dataset
print("=== DATASET ===")
print(df)

# Calcul de statistiques
moyenne = np.mean(ventes)
maximum = np.max(ventes)
minimum = np.min(ventes)
somme = np.sum(ventes)

# Affichage des résultats
print("\n=== ANALYSE ===")
print("Moyenne des ventes :", moyenne)
print("Vente maximale :", maximum)
print("Vente minimale :", minimum)
print("Somme totale :", somme)

# Création du graphique en barres
plt.bar(mois, ventes)

# Titre du graphique
plt.title("Ventes de la boutique par mois")

# Nom de l'axe X
plt.xlabel("Mois")

# Nom de l'axe Y
plt.ylabel("Ventes")

# Affichage du graphique
plt.show()