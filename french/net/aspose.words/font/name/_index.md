---
title: Font.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Nom de police pour personnaliser et définir facilement vos styles de police, améliorant ainsi l'attrait et la lisibilité de votre conception.
type: docs
weight: 230
url: /fr/net/aspose.words/font/name/
---
## Font.Name property

Obtient ou définit le nom de la police.

```csharp
public string Name { get; set; }
```

## Remarques

Lors de l'obtention, les retours[`NameAscii`](../nameascii/).

Lors du réglage, ensembles[`NameAscii`](../nameascii/) ,[`NameBi`](../namebi/) ,[`NameFarEast`](../namefareast/) et[`NameOther`](../nameother/) à la valeur spécifiée.

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
