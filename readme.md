# Analyseur de Sites WordPress

Un outil automatisé pour analyser les sites WordPress, permettant d'extraire des informations telles que la version de WordPress, les utilisateurs enregistrés et l'adresse IP associée au site. Ce script peut également compléter un rapport Word existant avec les données collectées.

## Fonctionnalités

- **Énumération des utilisateurs** : Récupère la liste des utilisateurs enregistrés sur le site WordPress cible.
- **Détection de la version de WordPress** : Identifie la version de WordPress utilisée par le site cible.
- **Récupération de l'adresse IP** : Obtient l'adresse IP associée au nom de domaine du site cible.
- **Génération de rapports** : Complète un document Word ou excel existant avec les informations collectées.

## Prérequis

Assurez-vous d'avoir les éléments suivants installés sur votre système :

- Python 3.x
- Les modules Python suivants :
  - `argparse`
  - `requests`
  - `re`
  - `urllib3`
  - `openpyxl`
  - `socket`
  - `python-docx`

Vous pouvez installer les modules requis en exécutant :

```bash
pip install requests urllib3 openpyxl python-docx
```
ou 
```bash
py -m install requests urllib3 openpyxl python-docx
```
## Installation
1. Clonez ce dépôt sur votre machine 
```bash
git clone https://github.com/lgutel/wordpress_detector.git
```
2. Accédez au répertoir du projet:
```bash
cd wordpress_detector
```
## Utilisation
Le script propose plusieurs options pour analyser un site WordPress ou traiter une liste de sites depuis un fichier. Voici quelques exemples d'utilisation :

Analyser un site spécifique :
```bash
python main.py -t exemple.com
```
Énumérer les utilisateurs d'un site :
```bash
python main.py -t exemple.com -ue
```
Obtenir la version de WordPress d'un site :
```bash
python main.py -t exemple.com -wv
```
Analyser une liste de sites depuis un fichier :
```bash
python main.py -if liste_sites.txt
```
Compléter un rapport Word avec les informations collectées :
```bash
python main.py -t exemple.com -do chemin/vers/rapport.docx
```
## Options

-t, --target : Spécifie l'URL du site WordPress à analyser.

-ue, --user-enumeration : Active l'énumération des utilisateurs du site cible.

-wv, --wordpress-version : Récupère la version de WordPress du site cible.

-if, --input-file : Spécifie un fichier contenant une liste d'URLs à analyser.

-do, --document-output : Spécifie le chemin vers un document Word à compléter avec les informations collectées.

## Avertissement

Cet outil est destiné à des fins éducatives uniquement. L'auteur ne saurait être tenu responsable de toute utilisation abusive de cet outil. Veuillez vous assurer que vous avez l'autorisation appropriée avant d'analyser un site web.
