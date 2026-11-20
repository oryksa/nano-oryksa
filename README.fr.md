# Nano ORYKSA

[![English](https://img.shields.io/badge/English-30363d?style=for-the-badge)](README.md) [![Português](https://img.shields.io/badge/Portugu%C3%AAs-30363d?style=for-the-badge)](README.pt.md) [![Español](https://img.shields.io/badge/Espa%C3%B1ol-30363d?style=for-the-badge)](README.es.md) [![Français](https://img.shields.io/badge/Fran%C3%A7ais-0891b2?style=for-the-badge)](README.fr.md)

**L'IA hors ligne de l'app mobile ORYKSA.**

Quand le téléphone perd le signal - dans un avion, dans un tunnel, dans une cave - l'assistant
ORYKSA ne s'éteint pas. Une version plus petite d'elle, **Nano ORYKSA**, prend le relais
depuis l'intérieur du téléphone. Elle est plus limitée que l'ORYKSA avec qui vous parlez en ligne,
mais elle porte la mémoire : votre profil, vos services, vos prix, vos horaires
d'ouverture et tout votre Brain.

Ce dépôt héberge les fichiers du modèle que l'app télécharge. Rien ici ne s'exécute sur un
serveur : tout est conçu pour s'exécuter sur le téléphone lui-même.

Développé par **Weslley Harakawa** - [ORYKSA](https://oryksa.com)

---

## Ce que Nano ORYKSA fait sans connexion

- Répond sur votre entreprise, à partir de la mémoire synchronisée avec le téléphone
- Note tout ce que vous lui demandez de modifier et l'exécute dès que vous êtes de nouveau en ligne
- Discute avec vous et vous aide à vous apaiser quand vous êtes stressé ou anxieux
- Donne les numéros d'urgence et les premiers secours de base, sans aucune connexion

## Ce qu'elle ne peut pas faire hors ligne

- Lire les nouveaux messages des clients (ils vivent sur le serveur)
- Réserver des rendez-vous ou modifier votre compte (ils vont dans une file d'attente)
- Chercher sur le web

Elle le dit clairement au lieu de faire semblant. Tout ce qui a besoin du serveur est mis en file d'attente
et exécuté, un par un, dès que le téléphone est de nouveau en ligne.

---

## Comment l'app choisit un cerveau

| Téléphone | Ce qui s'exécute | Téléchargement |
|---|---|---|
| iPhone 15 Pro et plus récents, iOS 26 avec Apple Intelligence | le modèle qu'Apple fournit déjà dans iOS | **aucun** |
| iPhone plus anciens et Android | le modèle publié dans ce dépôt | facultatif, à la demande |
| Tout autre appareil | recherche dans la mémoire, sans aucun modèle | aucun |

L'app ORYKSA dans les boutiques **n'embarque jamais de modèle**. Elle reste légère. L'IA hors ligne
n'est téléchargée que si le propriétaire la demande, et peut être supprimée à tout moment pour libérer
de l'espace.

## La mémoire

Avant que le signal ne disparaisse, l'app conserve une copie de tout ce que Nano ORYKSA a besoin de
savoir. C'est du texte, mesuré en kilo-octets, récupéré depuis `GET /api/app/offline-pack`
et actualisé automatiquement chaque fois que l'app s'ouvre ou revient à l'écran.

## Versions

Les fichiers du modèle sont publiés comme fichiers de version (release assets). L'app lit l'adresse de téléchargement
depuis le backend ORYKSA, de sorte que le modèle peut être remplacé ou désactivé sans
publier de nouvelle version de l'app.

| Fichier | Modèle | Taille | Format |
|---|---|---|---|
| `oryksa-nano.gguf` | Gemma 3 1B Instruct (Q4_K_M) | 778 MB | GGUF |

## Licence des modèles

Les poids des modèles publiés ici conservent la licence de leurs auteurs d'origine.
Gemma est distribué sous les [Gemma Terms of Use](https://ai.google.dev/gemma/terms)
de Google. Utiliser ce dépôt implique d'accepter ces conditions.

## À propos de l'auteur

**Weslley Harakawa** - Fondateur d'ORYKSA AI et Chief Innovation Officer chez Harakawa Tech. À Lisbonne, Portugal. Spécialités : intelligence artificielle, développement web et mobile, tokenisation blockchain. Formation : University of the People.

- Site web : https://harakawa.tech
- LinkedIn : https://www.linkedin.com/in/weslleyharakawa/
- Instagram : https://www.instagram.com/weslley.harakawa
- ORYKSA AI Employees : https://oryksa.com (X: https://x.com/oryksa, Instagram: https://www.instagram.com/oryksaai, YouTube: https://www.youtube.com/@ORYKSA)

Le nom, la marque et l'app ORYKSA sont la propriété de Weslley Harakawa.
