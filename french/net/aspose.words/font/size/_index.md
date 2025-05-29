---
title: Font.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words pour .NET
description: Ajustez facilement la taille de police grâce à la propriété Taille de police. Personnalisez votre texte en points pour une meilleure lisibilité et un design plus attrayant.
type: docs
weight: 350
url: /fr/net/aspose.words/font/size/
---
## Font.Size property

Obtient ou définit la taille de la police en points.

```csharp
public double Size { get; set; }
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

Montre comment insérer du texte formaté à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez le formatage de la police, puis ajoutez du texte.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
