---
title: MarkdownSaveOptions.ExportUnderlineFormatting
linktitle: ExportUnderlineFormatting
articleTitle: ExportUnderlineFormatting
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété MarkdownSaveOptions ExportUnderlineFormatting optimise vos exportations de texte. Contrôlez facilement le formatage du soulignement grâce à ce paramètre booléen.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/markdownsaveoptions/exportunderlineformatting/
---
## MarkdownSaveOptions.ExportUnderlineFormatting property

Obtient ou définit une valeur booléenne indiquant d'exporter le formatage du texte souligné sous forme de séquence de deux caractères plus "++". La valeur par défaut est`FAUX` .

```csharp
public bool ExportUnderlineFormatting { get; set; }
```

## Exemples

Montre comment exporter le formatage souligné au format ++.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Single;
builder.Write("Lorem ipsum. Dolor sit amet.");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

### Voir également

* class [MarkdownSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
