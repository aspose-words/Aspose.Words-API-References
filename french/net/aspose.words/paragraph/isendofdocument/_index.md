---
title: IsEndOfDocument
second_title: Référence de l'API Aspose.Words pour .NET
description: Vrai si ce paragraphe est le dernier paragraphe de la dernière section du document.
type: docs
weight: 60
url: /fr/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

Vrai si ce paragraphe est le dernier paragraphe de la dernière section du document.

```csharp
public bool IsEndOfDocument { get; }
```

### Exemples

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
// puis commence une nouvelle ligne, en ajoutant un nouveau paragraphe.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Voir également

* class [Paragraph](../../paragraph)
* espace de noms [Aspose.Words](../../paragraph)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
