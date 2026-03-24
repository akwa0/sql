# sql
# 📑 Fiche de Révision : SQL & Visual Studio (Exam 2026)

Ce guide récapitule les étapes essentielles pour créer, gérer et interroger une base de données SQL Server via l'IDE Visual Studio.

---

## 🛠 1. Configuration de l'Environnement
1. **Ouvrir l'Explorateur de serveurs** : `Affichage` > `Explorateur de serveurs`.
2. **Créer la Connexion** : Clic droit sur `Connexions de données` > `Ajouter une connexion`.
   - **Serveur** : `(localdb)\MSSQLLocalDB`
   - **Base** : Saisir un nom (ex: `ExamenDB`) et cliquer sur **OK** (Confirmer la création).
3. **Créer une Table** : Clic droit sur le dossier `Tables` > `Ajouter une nouvelle table`.

---

## 🏗 2. Design de la Table (T-SQL)
Dans l'onglet **Design**, n'oubliez pas les trois piliers :

* **Clé Primaire (PK)** : Clic droit sur la colonne > `Définir la clé primaire`.
* **Auto-Incrément (Identity)** : 
    - Fenêtre Propriétés > `Spécification de l'identité` > `(Is Identity)` = **True**.
* **Mise à jour (CRUCIAL)** : Cliquer sur le bouton **Mettre à jour** (Update) en haut à gauche, puis **Mettre à jour la base de données**.

### Exemple de script de création :
```sql
CREATE TABLE [dbo].[Clients] (
    [Id]    INT           IDENTITY (1, 1) NOT NULL,
    [Nom]   NVARCHAR (50) NOT NULL,
    [Email] NVARCHAR (50) NULL,
    PRIMARY KEY CLUSTERED ([Id] ASC)
);




