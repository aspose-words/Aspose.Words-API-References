---
title: MarkdownListExportMode Enum
linktitle: MarkdownListExportMode
articleTitle: MarkdownListExportMode
second_title: Aspose.Words для .NET
description: Узнайте, как перечисление MarkdownListExportMode от Aspose.Words улучшает экспорт списков в Markdown, обеспечивая точное форматирование и бесшовную интеграцию ваших документов.
type: docs
weight: 6040
url: /ru/net/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enumeration

Указывает, как списки экспортируются в Markdown.

```csharp
public enum MarkdownListExportMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| MarkdownSyntax | `0` | Экспорт элементов списка, совместимых с синтаксисом Markdown. |
| PlainText | `1` | Экспортировать элементы списка как обычный текст. |

## Примеры

Показывает, как список элементов будет записан в документ разметки.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Используйте MarkdownListExportMode.PlainText или MarkdownListExportMode.MarkdownSyntax для экспорта списка.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
