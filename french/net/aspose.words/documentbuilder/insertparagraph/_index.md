---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words pour .NET
description: Améliorez vos documents sans effort avec la méthode InsertParagraph de DocumentBuilder, permettant des sauts de paragraphe transparents pour une meilleure lisibilité.
type: docs
weight: 450
url: /fr/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Insère un saut de paragraphe dans le document.

```csharp
public Paragraph InsertParagraph()
```

### Return_Value

Le nœud de paragraphe qui vient d'être inséré. Il s'agit du même nœud que[`CurrentParagraph`](../currentparagraph/).

## Remarques

Formatage de paragraphe actuel spécifié par le[`ParagraphFormat`](../paragraphformat/) la propriété est utilisée.

Coupe le paragraphe actuel en deux. Après insertion du paragraphe, le curseur se place au début du nouveau paragraphe.

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

// La méthode « Writeln » termine le paragraphe après avoir ajouté du texte
// puis démarre une nouvelle ligne, ajoutant un nouveau paragraphe.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Voir également

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
