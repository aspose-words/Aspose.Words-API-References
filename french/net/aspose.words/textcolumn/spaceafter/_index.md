---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TextColumn SpaceAfter pour ajuster facilement l'espacement entre les colonnes de votre mise en page. Améliorez la lisibilité et le design avec précision !
type: docs
weight: 10
url: /fr/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Obtient ou définit l'espacement entre cette colonne et la suivante, en points. Non requis pour la dernière colonne.

```csharp
public double SpaceAfter { get; set; }
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
