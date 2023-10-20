---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words pour .NET
description: TextColumn SpaceAfter propriété. Obtient ou définit lespace entre cette colonne et la colonne suivante en points. Non requis pour la dernière colonne en C#.
type: docs
weight: 10
url: /fr/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Obtient ou définit l'espace entre cette colonne et la colonne suivante en points. Non requis pour la dernière colonne.

```csharp
public double SpaceAfter { get; set; }
```

## Exemples

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

* class [TextColumn](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
