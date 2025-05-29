---
title: MarkdownSaveOptions.EmptyParagraphExportMode
linktitle: EmptyParagraphExportMode
articleTitle: EmptyParagraphExportMode
second_title: Aspose.Words для .NET
description: Настройте экспорт пустых абзацев в Markdown с помощью Aspose.Words. Установите EmptyParagraphExportMode для оптимальной конвертации документа.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/
---
## MarkdownSaveOptions.EmptyParagraphExportMode property

Указывает, как экспортировать пустые абзацы в Markdown. Значение по умолчанию:EmptyLine .

```csharp
public MarkdownEmptyParagraphExportMode EmptyParagraphExportMode { get; set; }
```

## Примеры

Показывает, как экспортировать пустые абзацы.

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

### Смотрите также

* enum [MarkdownEmptyParagraphExportMode](../../markdownemptyparagraphexportmode/)
* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
