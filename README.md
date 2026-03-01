# 📄 Grist Document Template (Mail Merge) Widget

**Author / Auteur : Said Hamadou (HmD)**
**License / Licence : Apache-2.0**

---

## 🇫🇷 Français

Widget personnalisé Grist pour créer des documents avec des variables de champs, prévisualiser le publipostage et générer des PDF.

### Fonctionnalités

- **Éditeur WYSIWYG** : traitement de texte complet (gras, italique, titres, listes, tableaux, images...)
- **Variables de champs** : insérez des `{{Nom}}`, `{{Adresse}}` etc. depuis une table Grist
- **Import Word (.docx)** : importez un fichier Word en conservant le formatage
- **Prévisualisation** : naviguez enregistrement par enregistrement pour voir le document avec les vraies valeurs
- **Génération PDF** : exportez un PDF pour un enregistrement ou tous les enregistrements
- **Sauvegarde du modèle** : le modèle est sauvegardé localement par table
- **Bilingue FR/EN** : interface en français et anglais

### 🆕 Nouvelles fonctionnalités

#### Images dynamiques
- **Insertion d'images depuis une colonne** : utilisez `{{IMG:NomColonne}}` ou `{{IMG:NomColonne:largeur}}` pour insérer une image dont l'URL est stockée dans une colonne Grist
- **Formats supportés** : URLs web (https://...), Attachments Grist, chemins relatifs avec URL de base
- **Images dans les boucles** : chaque ligne de la boucle affiche sa propre image

#### Tableaux avancés
- **Mise en page (tablelayout)** : créez des colonnes côte à côte (2 colonnes, 3 colonnes, sidebar gauche/droite) pour disposer du contenu ou des tableaux côte à côte
- **Tableaux imbriqués (nestedtable)** : insérez un tableau à l'intérieur d'une cellule d'un autre tableau
- **Bordures de tableau (tableborder)** : personnalisez les bordures de tout le tableau (couleur, épaisseur, visibilité)
- **Bordures de cellule (cellborder)** : personnalisez les bordures d'une cellule spécifique (couleur, épaisseur, côtés individuels)
- **Largeur de colonne (columnwidth)** : définissez une largeur fixe pour une colonne (en px ou %)

#### Formatage
- **Texte vertical (verticaltext)** : orientez le texte verticalement dans une cellule
- **Saut de page (pagebreak)** : insérez un saut de page pour le PDF
- **Paragraphe après tableau (insertparagraph)** : ajoutez facilement un paragraphe après un tableau

#### Boucles et données liées
- **Boucles avec filtre** : `{{#each Colonne=Valeur}}...{{/each}}` pour afficher les lignes correspondant à un critère
- **Boucles sur tables liées** : `{{#each @NomTable.ColonneRef}}...{{/each}}` pour afficher les données d'une table liée

### Installation

1. Dans Grist, ajoutez un widget **Personnalisé**
2. URL : `https://isaytoo.github.io/grist-doc-template-widget/`
3. Niveau d'accès : **Accès complet au document**

### Utilisation

1. Sélectionnez une table source
2. Créez votre document dans l'éditeur (ou importez un fichier Word)
3. Cliquez sur les variables pour les insérer dans le document
4. Allez dans l'onglet **Prévisualisation** pour voir le résultat avec les vraies données
5. Allez dans l'onglet **Générer PDF** pour exporter

### Syntaxe des variables

| Syntaxe | Description |
|---------|-------------|
| `{{NomColonne}}` | Affiche la valeur de la colonne |
| `{{IMG:NomColonne}}` | Affiche une image depuis l'URL de la colonne |
| `{{IMG:NomColonne:150}}` | Affiche une image avec largeur de 150px |
| `{{#each}}...{{/each}}` | Boucle sur toutes les lignes |
| `{{#each Statut=Actif}}...{{/each}}` | Boucle filtrée sur les lignes où Statut=Actif |
| `{{#each @Commandes.Client}}...{{/each}}` | Boucle sur la table liée Commandes via la colonne Client |

---

## 🇬🇧 English

Custom Grist widget to create documents with field variables, preview mail merge and generate PDFs.

### Features

- **WYSIWYG editor**: full word processor (bold, italic, headings, lists, tables, images...)
- **Field variables**: insert `{{Name}}`, `{{Address}}` etc. from a Grist table
- **Word import (.docx)**: import a Word file preserving formatting
- **Preview**: navigate record by record to see the document with real values
- **PDF generation**: export a PDF for one record or all records
- **Template saving**: template is saved locally per table
- **Bilingual FR/EN**: French and English interface

### 🆕 New Features

#### Dynamic Images
- **Insert images from a column**: use `{{IMG:ColumnName}}` or `{{IMG:ColumnName:width}}` to insert an image whose URL is stored in a Grist column
- **Supported formats**: Web URLs (https://...), Grist Attachments, relative paths with base URL
- **Images in loops**: each row in the loop displays its own image

#### Advanced Tables
- **Layout (tablelayout)**: create side-by-side columns (2 columns, 3 columns, left/right sidebar) to arrange content or tables side by side
- **Nested tables (nestedtable)**: insert a table inside a cell of another table
- **Table borders (tableborder)**: customize borders for the entire table (color, thickness, visibility)
- **Cell borders (cellborder)**: customize borders for a specific cell (color, thickness, individual sides)
- **Column width (columnwidth)**: set a fixed width for a column (in px or %)

#### Formatting
- **Vertical text (verticaltext)**: orient text vertically in a cell
- **Page break (pagebreak)**: insert a page break for PDF
- **Paragraph after table (insertparagraph)**: easily add a paragraph after a table

#### Loops and Linked Data
- **Filtered loops**: `{{#each Column=Value}}...{{/each}}` to display rows matching a criterion
- **Loops on linked tables**: `{{#each @TableName.RefColumn}}...{{/each}}` to display data from a linked table

### Installation

1. In Grist, add a **Custom** widget
2. URL: `https://isaytoo.github.io/grist-doc-template-widget/`
3. Access level: **Full document access**

### Usage

1. Select a source table
2. Create your document in the editor (or import a Word file)
3. Click on variables to insert them into the document
4. Go to the **Preview** tab to see the result with real data
5. Go to the **Generate PDF** tab to export

### Variable Syntax

| Syntax | Description |
|--------|-------------|
| `{{ColumnName}}` | Display the column value |
| `{{IMG:ColumnName}}` | Display an image from the column URL |
| `{{IMG:ColumnName:150}}` | Display an image with 150px width |
| `{{#each}}...{{/each}}` | Loop over all rows |
| `{{#each Status=Active}}...{{/each}}` | Filtered loop on rows where Status=Active |
| `{{#each @Orders.Customer}}...{{/each}}` | Loop on linked table Orders via Customer column |
