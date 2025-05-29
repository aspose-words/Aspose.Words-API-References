---
title: ParagraphFormat.AddSpaceBetweenFarEastAndDigit
linktitle: AddSpaceBetweenFarEastAndDigit
articleTitle: AddSpaceBetweenFarEastAndDigit
second_title: Aspose.Words pour .NET
description: Optimisez la mise en page de votre document avec la propriété AddSpaceBetweenFarEastAndDigit, améliorant la lisibilité en ajustant l'espacement entre le texte et les nombres d'Asie de l'Est.
type: docs
weight: 20
url: /fr/net/aspose.words/paragraphformat/addspacebetweenfareastanddigit/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndDigit property

Obtient ou définit un indicateur indiquant si l'espacement entre les caractères est automatiquement ajusté entre les régions de nombres et les régions de texte d'Asie de l'Est dans le paragraphe actuel.

```csharp
public bool AddSpaceBetweenFarEastAndDigit { get; set; }
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
