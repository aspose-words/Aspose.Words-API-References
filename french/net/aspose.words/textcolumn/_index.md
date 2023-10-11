---
title: Class TextColumn
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.TextColumn classe. Représente une seule colonne de texte.TextColumn est membre duTextColumnCollection collection. LeTextColumn la collection inclut toutes les colonnes dune section dun document.
type: docs
weight: 6390
url: /fr/net/aspose.words/textcolumn/
---
## TextColumn class

Représente une seule colonne de texte.`TextColumn` est membre du[`TextColumnCollection`](../textcolumncollection/) collection. Le`TextColumn` la collection inclut toutes les colonnes d'une section d'un document.

Pour en savoir plus, visitez le[Travailler avec des sections](https://docs.aspose.com/words/net/working-with-sections/) article documentaire.

```csharp
public class TextColumn
```

## Propriétés

| Nom | La description |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Obtient ou définit l'espace entre cette colonne et la colonne suivante en points. Non requis pour la dernière colonne. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Obtient ou définit la largeur de la colonne de texte en points. |

### Remarques

`TextColumn` les objets ne sont utilisés que pour spécifier des colonnes avec une largeur et un espacement personnalisés. Si vous souhaitez que les colonnes du document soient de largeur égale, définissez TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) à`vrai`.

Quand un nouveau`TextColumn` est créé, sa largeur et son espacement sont définis sur zéro.

### Exemples

Montre comment créer des colonnes inégalement espacées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Détermine la quantité d'espace dont nous disposons pour organiser les colonnes.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Définit la première colonne pour qu'elle soit étroite.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Définit la deuxième colonne pour qu'elle occupe le reste de l'espace disponible dans les marges de la page.
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


