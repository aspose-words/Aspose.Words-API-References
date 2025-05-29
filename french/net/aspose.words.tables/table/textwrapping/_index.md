---
title: Table.TextWrapping
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words pour .NET
description: Découvrez la propriété « Table TextWrapping » pour gérer facilement l'enchaînement du texte dans vos tableaux. Améliorez la lisibilité et la conception grâce à des options de texte flexibles !
type: docs
weight: 310
url: /fr/net/aspose.words.tables/table/textwrapping/
---
## Table.TextWrapping property

Obtient ou définit`TextWrapping` pour la table.

```csharp
public TextWrapping TextWrapping { get; set; }
```

## Exemples

Montre comment travailler avec l'habillage du texte du tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Définissez la propriété « TextWrapping » sur « TextWrapping.Around » pour que le tableau enveloppe le texte autour d'elle,
// et poussez-le vers le bas dans le paragraphe ci-dessous en définissant la position.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Voir également

* enum [TextWrapping](../../textwrapping/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
