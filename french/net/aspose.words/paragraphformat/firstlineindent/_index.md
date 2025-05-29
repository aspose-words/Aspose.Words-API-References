---
title: ParagraphFormat.FirstLineIndent
linktitle: FirstLineIndent
articleTitle: FirstLineIndent
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la propriété ParagraphFormat FirstLineIndent pour personnaliser facilement les retraits de première ligne ou suspendus dans vos documents pour une meilleure lisibilité.
type: docs
weight: 120
url: /fr/net/aspose.words/paragraphformat/firstlineindent/
---
## ParagraphFormat.FirstLineIndent property

Obtient ou définit la valeur (en points) d'une première ligne ou d'un retrait suspendu.

Utilisez des valeurs positives pour définir le retrait de la première ligne et des valeurs négatives pour définir le retrait suspendu.

```csharp
public double FirstLineIndent { get; set; }
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
