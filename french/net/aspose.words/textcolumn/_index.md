---
title: TextColumn Class
linktitle: TextColumn
articleTitle: TextColumn
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.TextColumn pour gérer les colonnes de texte dans vos documents. Accédez et personnalisez facilement chaque colonne de votre section de texte.
type: docs
weight: 7240
url: /fr/net/aspose.words/textcolumn/
---
## TextColumn class

Représente une seule colonne de texte.`TextColumn` est membre de la[`TextColumnCollection`](../textcolumncollection/) collection. Le`TextColumn`la collection comprend toutes les colonnes d'une section d'un document.

Pour en savoir plus, visitez le[Travailler avec des sections](https://docs.aspose.com/words/net/working-with-sections/) article de documentation.

```csharp
public class TextColumn
```

## Propriétés

| Nom | La description |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Obtient ou définit l'espacement entre cette colonne et la suivante, en points. Non requis pour la dernière colonne. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Obtient ou définit la largeur de la colonne de texte en points. |

## Remarques

`TextColumn` Les objets servent uniquement à spécifier des colonnes avec une largeur et un espacement personnalisés. Pour que les colonnes du document aient la même largeur, définissez TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) à`vrai`.

Lorsqu'un nouveau`TextColumn` est créé, sa largeur et son espacement sont définis sur zéro.

## Exemples

Montre comment créer des colonnes espacées de manière inégale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Déterminez la quantité d'espace dont nous disposons pour organiser les colonnes.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Définissez la première colonne comme étant étroite.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Définissez la deuxième colonne pour qu'elle occupe le reste de l'espace disponible dans les marges de la page.
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
