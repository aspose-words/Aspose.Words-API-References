---
title: MarkdownEmptyParagraphExportMode Enum
linktitle: MarkdownEmptyParagraphExportMode
articleTitle: MarkdownEmptyParagraphExportMode
second_title: .NET için Aspose.Words
description: Aspose.Words'ün Markdown dışa aktarımında boş paragrafları nasıl işlediğini öğrenin. MarkdownEmptyParagraphExportMode enum'uyla biçimlendirmeyi kontrol edin.
type: docs
weight: 6010
url: /tr/net/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enumeration

Aspose.Words'ün boş paragrafları Markdown'a nasıl aktaracağını belirtir.

```csharp
public enum MarkdownEmptyParagraphExportMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| EmptyLine | `0` | Boş satırlar olarak dışa aktar. |
| MarkdownHardLineBreak | `1` | Markdown HardLineBreak karakteri '\' olarak dışa aktar. |
| None | `2` | Boş paragrafları dışa aktarmayın. |

## Örnekler

Boş paragrafların nasıl dışa aktarılacağını gösterir.

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

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
