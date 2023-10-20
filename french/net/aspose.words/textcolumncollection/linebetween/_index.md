---
title: TextColumnCollection.LineBetween
linktitle: LineBetween
articleTitle: LineBetween
second_title: Aspose.Words pour .NET
description: TextColumnCollection LineBetween propriété. Quandvrai ajoute une ligne verticale entre les colonnes en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

Quand`vrai` ajoute une ligne verticale entre les colonnes.

```csharp
public bool LineBetween { get; set; }
```

## Exemples

Montre comment séparer les colonnes par une ligne verticale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configure l'objet PageSetup de la section actuelle pour diviser le texte en plusieurs colonnes.
// Définissez la propriété "LineBetween" sur "true" pour mettre une ligne de séparation entre les colonnes.
// Définissez la propriété "LineBetween" sur "false" pour laisser l'espace entre les colonnes vide.
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.LineBetween = lineBetween;
columns.SetCount(3);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 3.");

doc.Save(ArtifactsDir + "PageSetup.VerticalLineBetweenColumns.docx");
```

### Voir également

* class [TextColumnCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
