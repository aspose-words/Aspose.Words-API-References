---
title: MarkdownEmptyParagraphExportMode Enum
linktitle: MarkdownEmptyParagraphExportMode
articleTitle: MarkdownEmptyParagraphExportMode
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie Aspose.Words leere Absätze im Markdown-Export verarbeitet. Steuern Sie die Formatierung mit der Aufzählung MarkdownEmptyParagraphExportMode.
type: docs
weight: 6010
url: /de/net/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enumeration

Gibt an, wie Aspose.Words leere Absätze nach Markdown exportiert.

```csharp
public enum MarkdownEmptyParagraphExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| EmptyLine | `0` | Als leere Zeilen exportieren. |
| MarkdownHardLineBreak | `1` | Exportieren als Markdown HardLineBreak-Zeichen '\'. |
| None | `2` | Keine leeren Absätze exportieren. |

## Beispiele

Zeigt, wie leere Absätze exportiert werden.

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

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
