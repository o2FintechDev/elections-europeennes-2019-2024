# Analyse et Visualisation des Résultats des Élections Européennes 2019–2024

Ce projet a pour objectif d’analyser l’évolution du paysage électoral français entre les élections européennes de **2019** et de **2024**.  
À l’aide de **Python**, il propose une exploration **géographique et interactive** des résultats par région, mettant en évidence les dynamiques politiques et territoriales.

Les visualisations interactives (réalisées avec **Plotly** et **GeoPandas**) permettent d’examiner les tendances du vote entre zones métropolitaines, périurbaines et rurales.

---

## Objectifs du projet

- Étudier la **stabilité du corps électoral** entre 2019 et 2024  
- Comparer les **taux de participation** et les **suffrages exprimés** par région  
- Visualiser la **répartition géographique** des principales listes électorales  
- Mettre en évidence la **bipolarisation** entre vote métropolitain et vote périphérique  

---

## Technologies et bibliothèques utilisées

- **Python 3.11+**
- **pandas**, **numpy** → manipulation et analyse de données  
- **geopandas** → traitement des données géographiques et GeoJSON  
- **plotly.express**, **plotly.graph_objects** → visualisations interactives et cartes choroplèthes  
- **jupyterlab** → environnement de travail pour notebooks interactifs  

---

## Installation
```bash
git clone https://github.com/o2FintechDev/elections-europeennes-fr-2019-2024.git

cd E:/elections-fr-2019-2024
pip install -r requirements.txt
