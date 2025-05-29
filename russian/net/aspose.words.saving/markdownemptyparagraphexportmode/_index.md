---
title: MarkdownEmptyParagraphExportMode Enum
linktitle: MarkdownEmptyParagraphExportMode
articleTitle: MarkdownEmptyParagraphExportMode
second_title: Aspose.Words для .NET
description: Узнайте, как Aspose.Words обрабатывает пустые абзацы в экспорте Markdown. Управляйте форматированием с помощью перечисления MarkdownEmptyParagraphExportMode.
type: docs
weight: 6010
url: /ru/net/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enumeration

Указывает, как Aspose.Words экспортирует пустые абзацы в Markdown.

```csharp
public enum MarkdownEmptyParagraphExportMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| EmptyLine | `0` | Экспортировать как пустые строки. |
| MarkdownHardLineBreak | `1` | Экспортировать как символ Markdown HardLineBreak '\'. |
| None | `2` | Не экспортировать пустые абзацы. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
