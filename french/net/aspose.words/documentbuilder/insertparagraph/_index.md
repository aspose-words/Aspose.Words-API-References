---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words pour .NET
description: DocumentBuilder InsertParagraph méthode. Insère un saut de paragraphe dans le document en C#.
type: docs
weight: 420
url: /fr/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Insère un saut de paragraphe dans le document.

```csharp
public Paragraph InsertParagraph()
```

### Return_Value

Le nœud de paragraphe qui vient d'être inséré. C'est le même nœud que[`CurrentParagraph`](../currentparagraph/).

## Remarques

Formatage actuel du paragraphe spécifié par le[`ParagraphFormat`](../paragraphformat/) la propriété est utilisée.

Coupe le paragraphe actuel en deux. Après avoir inséré le paragraphe, le curseur est placé au début du nouveau paragraphe.

Une exception est levée s'il n'est pas possible d'insérer un saut de paragraphe à la position actuelle du curseur.

## Exemples

Montre comment insérer un paragraphe dans le document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// La méthode "Writeln" termine le paragraphe après avoir ajouté du texte
// puis commence une nouvelle ligne, ajoutant un nouveau paragraphe.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Voir également

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
