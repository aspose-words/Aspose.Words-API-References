---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font HighlightColor : personnalisez facilement la couleur de surbrillance de votre texte pour une meilleure lisibilité et un meilleur attrait visuel. Sublimez votre design !
type: docs
weight: 150
url: /fr/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Obtient ou définit la couleur de surbrillance (marqueur).

```csharp
public Color HighlightColor { get; set; }
```

## Exemples

Montre comment formater une série de texte à l'aide de sa propriété de police.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
