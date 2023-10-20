---
title: TextWrapping Enum
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words pour .NET
description: Aspose.Words.Tables.TextWrapping énumération. Spécifie comment le texte est enroulé autour du tableau en C#.
type: docs
weight: 6380
url: /fr/net/aspose.words.tables/textwrapping/
---
## TextWrapping enumeration

Spécifie comment le texte est enroulé autour du tableau.

```csharp
public enum TextWrapping
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Le texte et le tableau sont affichés dans l'ordre de leur apparition dans le document. |
| Around | `1` | Le texte est enroulé autour du tableau occupant l'espace latéral disponible. |
| Default | `0` | Valeur par défaut. |

## Exemples

Montre comment utiliser l'habillage du texte d'un tableau.

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

// Définissez la propriété "TextWrapping" sur "TextWrapping.Around" pour que le tableau enroule le texte autour de lui,
// et poussez-le vers le bas dans le paragraphe ci-dessous en définissant la position.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Voir également

* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)
