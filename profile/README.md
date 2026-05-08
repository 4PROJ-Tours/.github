# SUPFILE

SUPFILE est une plateforme de stockage cloud grand public, développée dans le cadre du projet de fin d'année de M1 à SUPINFO campus de Tours.

L'objectif : concevoir une alternative à Dropbox ou Google Drive, permettant à chaque utilisateur de stocker, organiser, prévisualiser et partager ses fichiers depuis n'importe quel appareil.

**L'application est disponible en ligne : [https://supfile.cloud](https://supfile.cloud)**

---

## Equipe

| Membre   | Role                 |
| -------- | -------------------- |
| **Enzo** | Frontend — UX/UI     |
| **Loïc** | Full Stack           |
| **Paul** | Backend — DevOps     |

---

## Fonctionnalites

- Inscription et connexion (email/mot de passe + OAuth2)
- Gestionnaire de fichiers avec arborescence de dossiers (breadcrumbs, drag & drop)
- Upload avec barre de progression, corbeille avec restauration
- Telechargement de dossiers complets en ZIP genere a la volee
- Previsualisation integree : images, PDF, textes, streaming audio/video
- Partage par lien public (avec expiration et mot de passe optionnels)
- Partage de dossier entre utilisateurs de la plateforme
- Recherche avec filtres par type et date
- Dashboard : quota utilise, graphique de repartition, fichiers recents
- Parametres utilisateur : avatar, email, mot de passe, theme clair/sombre

---

## Stack technique

### Web App

| Couche            | Technologie                      |
| ----------------- | -------------------------------- |
| Frontend          | Nuxt 4 + Vue 3 + TypeScript      |
| Etat              | Pinia                            |
| i18n              | vue-i18n                         |
| CSS               | Bootstrap 5                      |
| Backend           | NestJS 11 + TypeScript           |
| Base de donnees   | PostgreSQL 16                    |
| Stockage objets   | MinIO (S3-compatible)            |
| Auth              | JWT + bcrypt + OAuth2            |
| Reverse proxy     | Nginx 1.27 + TLS (Let's Encrypt) |
| Conteneurisation  | Docker + Docker Compose          |
| CI/CD             | Github Action                    |

### Mobile

L'application mobile est developpee avec **Capacitor** (sur base Vue), permettant de partager la logique metier avec le frontend web et de generer des builds natifs iOS et Android depuis une seule base de code.
