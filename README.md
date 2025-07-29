# 🚲 Cyclistic Bike-Share Data Analysis – Conversion & Implantation Stratégique

Ce projet explore les données d'utilisation du service de vélos partagés **Cyclistic**, à Chicago, afin d’aider l’entreprise à **convertir les cyclistes occasionnels en membres annuels** et à **optimiser l’implantation de nouvelles stations**.

---

## 🎯 Objectifs du projet

1. **Analyser les différences de comportement entre membres et cyclistes occasionnels**
2. **Identifier les moments et lieux d’usage les plus stratégiques**
3. **Recommander des actions marketing ciblées pour augmenter le taux d’abonnement**
4. **Déterminer les meilleurs emplacements pour implanter de nouvelles stations**

---

## 🛠️ Outils utilisés

- **Python (Pandas, Seaborn, Matplotlib)** – Nettoyage, enrichissement des données, visualisations exploratoires
- **Power BI** – Tableau de bord interactif avec KPIs, cartes, filtres dynamiques
- **Jupyter Notebook (VSCode)** – Préparation des analyses et graphiques statistiques

---

## 📊 Dashboard Power BI

📸  
<img width="1443" height="847" alt="image" src="https://github.com/user-attachments/assets/658dd611-64b2-4361-8675-01ca3f60d95b" />

<img width="1448" height="847" alt="image" src="https://github.com/user-attachments/assets/5f8be704-827b-4d1b-bc15-da86079f1926" />

<img width="1446" height="845" alt="image" src="https://github.com/user-attachments/assets/8cf62f03-81a7-4672-b78f-76472c78b4d5" />

<img width="1441" height="846" alt="image" src="https://github.com/user-attachments/assets/ce562810-3490-4060-8a85-c6b3018f43a3" />


*Le tableau de bord permet d'explorer :*
- Les comportements d’usage par type d’utilisateur et de vélo
- Les tendances temporelles (jours, heures, saisons)
- Les stations les plus sollicitées
- Une carte interactive des départs / arrivées

---

## 🧪 Datasets utilisés

📦 **Cyclistic Bike Share Trip Data – Janvier 2021**

- Données publiques de trajets partagés à Chicago (5,8M lignes initiales)
- Enrichissement : durée, distance, jour, heure, saison, type de trajet, coordonnées GPS, nom de station
```
####### Importation des datasets depuis le serveur AWS dédié

# Liste des noms de fichiers
file_names = [
    "202101-divvy-tripdata.zip",
    "202102-divvy-tripdata.zip",
    "202103-divvy-tripdata.zip",
    "202104-divvy-tripdata.zip",
    "202105-divvy-tripdata.zip",
    "202106-divvy-tripdata.zip",
    "202107-divvy-tripdata.zip",
    "202108-divvy-tripdata.zip",
    "202109-divvy-tripdata.zip",
    "202110-divvy-tripdata.zip",
    "202111-divvy-tripdata.zip",
    "202112-divvy-tripdata.zip"
]

# URL de base
base_url = "https://divvy-tripdata.s3.amazonaws.com/"

# Télécharger chaque fichier
for file_name in file_names:

    url = base_url + file_name
    response = requests.get(url)

    # Extraire le fichier Zip dans le dossier local "wild_divvy_data"
    with zipfile.ZipFile(io.BytesIO(response.content)) as the_zip:
      the_zip.extractall("wild_divvy_data")
```
---

## 💡 Résultats clés

- Les **cyclistes occasionnels** utilisent principalement les vélos **en été et le week-end**, avec des trajets plus longs
- Les **membres annuels** roulent **toute l’année, en semaine, en horaires de bureau**
- Des zones touristiques à fort potentiel n’ont pas encore de station (ex : Museum Campus)
- Le service peut maximiser ses conversions via des **abonnements saisonniers** et une **stratégie de présence géographique ciblée**

---

## 🧭 Auteur

👤 Réalisé par Yanis R. – Analyste Junior Data & BI  
Projet présenté dans le cadre d’un **cas d’usage marketing & business intelligence**.

---
