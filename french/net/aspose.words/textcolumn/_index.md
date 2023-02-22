---
title: Class TextColumn
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.TextColumn classe. Représente une seule colonne de texte. Colonne de texte est membre de laTextColumnCollection collection. La Colonnes de texte collection inclut toutes les colonnes dune section dun document.
type: docs
weight: 6090
url: /fr/net/aspose.words/textcolumn/
---
## TextColumn class

Représente une seule colonne de texte. **Colonne de texte** est membre de la[`TextColumnCollection`](../textcolumncollection/) collection. La **Colonnes de texte** collection inclut toutes les colonnes d'une section d'un document.

```csharp
public class TextColumn
```

## Propriétés

| Nom | La description |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Obtient ou définit l'espace entre cette colonne et la colonne suivante en points. Non requis pour la dernière colonne. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Obtient ou définit la largeur de la colonne de texte en points. |

### Remarques

**Colonne de texte** les objets ne sont utilisés que pour spécifier des colonnes avec une largeur et un espacement personnalisés. Si vous voulez que les colonnes du document aient la même largeur, définissez TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) à **vrai**.

Quand un nouveau **Colonne de texte** est créé, sa largeur et son espacement sont définis sur zéro.

### Exemples

Montre comment créer des colonnes espacées de manière inégale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Déterminer la quantité d'espace dont nous disposons pour organiser les colonnes.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Définit la première colonne comme étant étroite.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Définissez la deuxième colonne pour occuper le reste de l'espace disponible dans les marges de la page.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


