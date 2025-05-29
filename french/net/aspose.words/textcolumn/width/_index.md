---
title: TextColumn.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words pour .NET
description: Ajustez la propriété Largeur de la colonne de texte pour personnaliser facilement la largeur de votre colonne de texte en points pour un contrôle de mise en page et une lisibilité améliorés.
type: docs
weight: 20
url: /fr/net/aspose.words/textcolumn/width/
---
## TextColumn.Width property

Obtient ou définit la largeur de la colonne de texte en points.

```csharp
public double Width { get; set; }
```

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

* class [TextColumn](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
