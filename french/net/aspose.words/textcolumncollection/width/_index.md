---
title: TextColumnCollection.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Largeur de TextColumnCollection. Gérez facilement des colonnes uniformément espacées pour une mise en page et un design optimaux dans vos projets.
type: docs
weight: 60
url: /fr/net/aspose.words/textcolumncollection/width/
---
## TextColumnCollection.Width property

Lorsque les colonnes sont régulièrement espacées, obtient la largeur des colonnes.

```csharp
public double Width { get; }
```

## Remarques

N'a d'effet que lorsque[`EvenlySpaced`](../evenlyspaced/) est réglé sur`vrai`.

## Exemples

Montre comment créer plusieurs colonnes régulièrement espacées dans une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Voir également

* class [TextColumnCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
