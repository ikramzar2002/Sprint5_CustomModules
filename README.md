#  Hello World - Module Drupal

## Description
Le module **Hello World** est un module personnalisé pour **Drupal 10/11** qui permet d'afficher un simple message "Hello, World!" sur une page dédiée et dans un bloc.

---

##  Installation

###  **Via l'interface Drupal**
1. **Télécharge le module** et place-le dans `web/modules/custom/`
2. **Va dans l'administration Drupal** : `Extend` (admin/modules)
3. **Coche** "Hello World"
4. **Clique sur** "Install"

###  **Via Drush**
```bash
drush en hello_world -y 
```
![Capture d’écran]([https://i.imgur.com/mon-image.png](https://imgur.com/a/4m7Sbmv))

# Step 4:

## 1. Désinstaller et réinstaller le module:

## Résultat :

Désinstallation : le module est bien désactivé et supprimé de la base de données.
Réinstallation : tous les fichiers de configuration sont restaurés automatiquement.

## 2. Changer core_version_requirement à une version inférieure

## Résultat :

Drupal affiche un avertissement indiquant que la version du module ne correspond pas à celle du Core.
Le module ne peut pas être activé si la version de Drupal est trop récente.

## 3. Ajouter workflows comme dépendance

## Résultat :

Si le module Workflows n'est pas installé, Drupal affiche une erreur de dépendance et empêche l’installation de hello_world.
Après installation de workflows, hello_world peut être activé sans problème.

## 4. Ajouter un fichier composer.json

## Résultat :

composer.lock est généré.
Les dépendances sont bien installées.
Erreur si workflows ne peut pas être trouvé (problème de version).

## 5. Supprimer ou déplacer le module

## Résultat :

Erreur dans l'interface Drupal :
Le module est toujours référencé dans la base de données.
Affichage d'un message d'erreur indiquant que les fichiers sont manquants.
