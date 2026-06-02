# TP Android : Application de Gestion de Notes avec Room Database

## Présentation

Cette application Android développée en Java illustre l'utilisation d'une base de données locale moderne à l'aide de Room Persistence Library.

L’objectif du projet est d’apprendre comment stocker, récupérer et manipuler des données locales tout en respectant une architecture Android moderne.

---

# Objectifs pédagogiques

Ce projet permet de comprendre :

- la persistance locale sous Android ;
- l’utilisation de Room Database ;
- l’architecture Repository + ViewModel ;
- la gestion du cycle de vie des données ;
- l’utilisation du modèle MVVM.

---

# Fonctionnalités principales

## Gestion des notes

L’application offre les fonctionnalités suivantes :

- Ajouter une note
- Supprimer une note
- Afficher la liste des notes
- Supprimer toutes les notes
- Stockage permanent des données

---

# Structure des données

Chaque note possède :

| Attribut | Description |
|----------|----------|
| ID | Identifiant généré automatiquement |
| Title | Titre de la note |
| Description | Contenu de la note |

---

# Architecture utilisée

L’application adopte une architecture séparée en plusieurs couches.

```text
com.example.notesapp

├── data
│   ├── local
│   │   ├── Note.java
│   │   ├── NoteDao.java
│   │   └── NoteDatabase.java
│   │
│   └── NoteRepository.java
│
├── ui
│   ├── MainActivity.java
│   ├── NoteAdapter.java
│   └── NoteViewModel.java
│
└── viewmodel
    └── NoteViewModel.java
```

---

# Technologies utilisées

| Technologie | Utilisation |
|------------|------------|
| Java | Développement Android |
| Room Database | Base de données locale |
| LiveData | Mise à jour automatique des données |
| ViewModel | Gestion du cycle de vie |
| RecyclerView | Affichage des listes |
| MVVM | Architecture du projet |

---

# Base de données Room

L'application utilise trois composants principaux :

## Entity

Représente la structure d’une note.

```java
@Entity(tableName="notes_table")
class Note
```

## DAO

Contient les opérations sur la base :

- insertion
- suppression
- récupération
- suppression globale

## Database

Point central permettant l’accès aux données.

---

# Interface utilisateur

L’application possède :

- une interface simple et moderne ;
- une liste dynamique de notes ;
- des interactions rapides ;
- un affichage automatique après modification.

---

# Fonctionnement

## Ajout d’une note

L’utilisateur :

1. saisit un titre ;
2. ajoute une description ;
3. valide l’ajout.

La note est automatiquement enregistrée.

---

## Affichage

Les données sont :

- récupérées depuis Room ;
- observées grâce à LiveData ;
- affichées automatiquement.

---

## Suppression

L’application permet :

- supprimer une note ;
- supprimer toutes les notes.

---

# Résultats obtenus

Fonctionnalités réalisées :

- ✅ Base de données locale opérationnelle
- ✅ Architecture MVVM
- ✅ Persistance des données
- ✅ Gestion dynamique des listes
- ✅ Utilisation de Room Database
- ✅ Application Android complète

---

# Conclusion

Ce projet constitue une introduction pratique au développement Android moderne utilisant Room et MVVM afin de construire des applications capables de gérer efficacement des données locales.

---

# Auteur

AIT HMAD OUSSAMA
