---
title: TextColumnCollection.EvenlySpaced
linktitle: EvenlySpaced
articleTitle: EvenlySpaced
second_title: Aspose.Words pour .NET
description: Découvrez la propriété EvenlySpaced de TextColumnCollection, qui garantit des colonnes de texte de largeur égale pour une mise en page claire et organisée. Améliorez votre design sans effort !
type: docs
weight: 20
url: /fr/net/aspose.words/textcolumncollection/evenlyspaced/
---
## TextColumnCollection.EvenlySpaced property

Vrai si les colonnes de texte sont de largeur égale et régulièrement espacées.

```csharp
public bool EvenlySpaced { get; set; }
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

* class [TextColumnCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
