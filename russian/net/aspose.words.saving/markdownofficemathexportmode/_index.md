---
title: MarkdownOfficeMathExportMode Enum
linktitle: MarkdownOfficeMathExportMode
articleTitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words для .NET
description: Узнайте, как Aspose.Words.Saving.MarkdownOfficeMathExportMode улучшает экспорт OfficeMath в Markdown, обеспечивая точное и эффективное преобразование документов.
type: docs
weight: 6050
url: /ru/net/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enumeration

Указывает, как Aspose.Words экспортирует OfficeMath в Markdown.

```csharp
public enum MarkdownOfficeMathExportMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Text | `0` | Экспортировать OfficeMath как обычный текст. |
| Image | `1` | Экспортировать OfficeMath как изображение. |
| MathML | `2` | Экспортировать OfficeMath как MathML. |

## Примеры

Показывает, как OfficeMath будет записан в документ.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
