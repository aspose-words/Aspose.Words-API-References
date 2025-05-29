---
title: MarkdownEmptyParagraphExportMode Enum
linktitle: MarkdownEmptyParagraphExportMode
articleTitle: MarkdownEmptyParagraphExportMode
second_title: Aspose.Words pour .NET
description: Découvrez comment Aspose.Words gère les paragraphes vides lors de l'exportation Markdown. Contrôlez la mise en forme avec l'énumération MarkdownEmptyParagraphExportMode.
type: docs
weight: 6010
url: /fr/net/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enumeration

Spécifie comment Aspose.Words exporte les paragraphes vides vers Markdown.

```csharp
public enum MarkdownEmptyParagraphExportMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| EmptyLine | `0` | Exporter sous forme de lignes vides. |
| MarkdownHardLineBreak | `1` | Exporter en tant que caractère de saut de ligne dur Markdown '\'. |
| None | `2` | N'exportez pas les paragraphes vides. |

## Exemples

Montre comment exporter des paragraphes vides.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("First");
builder.Writeln("\r\n\r\n\r\n");
builder.Writeln("Last");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.EmptyParagraphExportMode = exportMode;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.EmptyParagraphExportMode.md", saveOptions);

string result = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.EmptyParagraphExportMode.md");

switch (exportMode)
{
    case MarkdownEmptyParagraphExportMode.None:
        Assert.AreEqual("First\r\n\r\nLast\r\n", result);
        break;
    case MarkdownEmptyParagraphExportMode.EmptyLine:
        Assert.AreEqual("First\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n", result);
        break;
    case MarkdownEmptyParagraphExportMode.MarkdownHardLineBreak:
        Assert.AreEqual("First\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n<br>\r\n", result);
        break;
}
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
