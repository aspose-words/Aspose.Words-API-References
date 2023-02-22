---
title: Font.HighlightColor
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Obtient ou définit la couleur de surbrillance marqueur.
type: docs
weight: 150
url: /fr/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Obtient ou définit la couleur de surbrillance (marqueur).

```csharp
public Color HighlightColor { get; set; }
```

### Exemples

Montre comment formater une suite de texte à l'aide de sa propriété de police.

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
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


