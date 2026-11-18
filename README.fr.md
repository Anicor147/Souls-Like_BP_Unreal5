# Souls-like

*[English version](README.md)*

Jeu d'action à la troisième personne inspiré des Souls : explore un donjon et un monde ouvert, affronte des chevaliers en patrouille et un boss.
Projet académique solo réalisé avec **Unreal Engine 5.3** et des **Blueprints** (février – mars 2024).

## Fonctionnalités

- **Combat au corps à corps et à distance** : combo à l'épée, arc, blocage au bouclier et roulade. Le joueur change d'arme en partie, et une machine à états d'animation gère les déplacements et les attaques de chaque arme.
- **Ennemis en patrouille** : le chevalier doré est piloté par un Behavior Tree et un Blackboard. Il se déplace entre des points de patrouille, poursuit le joueur quand il le voit et reprend sa patrouille quand il le perd.
- **Verrouillage de cible** sur un ennemi, barres de vie des ennemis et confirmation des coups.
- **Boss** avec barre de vie, au moins deux attaques et une phase d'enrage.
- **Énigme des lanternes** : il faut allumer les lanternes dans le bon ordre pour débloquer une porte, et une mauvaise séquence réinitialise l'énigme.
- **Système d'interaction** : un Blueprint parent commun à tous les objets interactifs, avec invite de touche à l'écran et effet visuel.
- **Inventaire** : armes à ramasser et potions de soin, conservés entre les niveaux.
- **Séquence de mort** : animation, puis écran de mort pour recommencer ou revenir au menu.
- **Trois cartes** : menu principal, donjon intérieur construit avec Cube Grid, et monde extérieur créé avec Landscape et Gaea, avec des décors de Quixel Bridge.
- **Interface** : vie et ressources, menu pause, invite d'interaction.

## Structure du projet

| Dossier | Contenu |
| --- | --- |
| `Content/Blueprints/Character` | Personnage joueur, mode de jeu, énumération des armes |
| `Content/Blueprints/Boss` | Boss |
| `Content/Blueprints/Interaction` | Classe parente d'interaction et interaction des lanternes |
| `Content/Assets/Enemy/GoldKnight/Blueprints` | Chevalier doré : contrôleur d'IA, Behavior Tree, Blackboard, barre de vie |
| `Content/Assets/Player_Character/Animations` | Animation Blueprint et montages (combo, blocage, roulade, potion, tir) |
| `Content/UI` | HUD, menu principal, menu pause, écran de mort, invite d'interaction |
| `Content/ThirdPerson/Maps` | `MainMenu`, `ThirdPersonMap` (donjon), `OpenWorld` |

## Lancer le projet

1. Installer **Unreal Engine 5.3**.
2. Ouvrir `MidtermProject/MidtermProject.uproject`.
3. Ouvrir la carte `MainMenu` et appuyer sur Play.

<details>
<summary>Exigences du travail</summary>

| Critère | Complété |
| --- | --- |
| 3 cartes ou plus : menu principal, niveau intérieur (donjon), niveau extérieur (monde ouvert) | ✓ |
| Interface : PV du joueur, ressources, menu pause | ✓ |
| Ennemi qui patrouille : se déplace entre des points, poursuit le joueur s'il le voit, revient en patrouille | ✓ |
| Énigme de type lanterne : porte à débloquer, objets interactifs, activation dans le bon ordre, réinitialisation si mauvaise séquence | ✓ |
| Boss : affichage des PV, mécanique d'enrage, au moins 2 attaques | ✓ |
| Séquence de mort : animation, transition vers l'écran de mort, option pour recommencer ou revenir au menu | ✓ |
| Système d'interaction : objets interactifs, effet visuel, touche clavier ou manette | ✓ |
| Inventaire : acquisition d'arme, objets de soin, conservation de l'inventaire | ✓ |
| Environnement : Cube Grid à l'intérieur, Landscape et Gaea à l'extérieur, décors Quixel Bridge | ✓ |
| Système de combat : combos au corps à corps, attaque à distance, action défensive | ✓ |

</details>
