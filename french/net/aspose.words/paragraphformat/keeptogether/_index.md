---
title: ParagraphFormat.KeepTogether
linktitle: KeepTogether
articleTitle: KeepTogether
second_title: Aspose.Words pour .NET
description: Découvrez la propriété KeepTogether de ParagraphFormat, assurez-vous que toutes les lignes restent ensemble sur une seule page pour une meilleure lisibilité du document et une présentation professionnelle.
type: docs
weight: 160
url: /fr/net/aspose.words/paragraphformat/keeptogether/
---
## ParagraphFormat.KeepTogether property

Vrai si toutes les lignes du paragraphe doivent rester sur la même page.

```csharp
public bool KeepTogether { get; set; }
```

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

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
