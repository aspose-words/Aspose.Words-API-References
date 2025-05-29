---
title: MarkdownSaveOptions.EmptyParagraphExportMode
linktitle: EmptyParagraphExportMode
articleTitle: EmptyParagraphExportMode
second_title: Aspose.Words pour .NET
description: Configurez l'exportation de paragraphes vides en Markdown avec Aspose.Words. Définissez EmptyParagraphExportMode pour une conversion optimale du document.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/
---
## MarkdownSaveOptions.EmptyParagraphExportMode property

Spécifie comment exporter les paragraphes vides vers Markdown. La valeur par défaut estEmptyLine .

```csharp
public MarkdownEmptyParagraphExportMode EmptyParagraphExportMode { get; set; }
```

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

* enum [MarkdownEmptyParagraphExportMode](../../markdownemptyparagraphexportmode/)
* class [MarkdownSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
