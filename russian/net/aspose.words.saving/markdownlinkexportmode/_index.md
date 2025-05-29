---
title: MarkdownLinkExportMode Enum
linktitle: MarkdownLinkExportMode
articleTitle: MarkdownLinkExportMode
second_title: Aspose.Words для .NET
description: Узнайте, как перечисление Aspose.Words MarkdownLinkExportMode улучшает экспорт ссылок в Markdown, легко оптимизируя процесс преобразования документов.
type: docs
weight: 6030
url: /ru/net/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enumeration

Указывает, как ссылки экспортируются в Markdown.

```csharp
public enum MarkdownLinkExportMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Auto | `0` | Автоматически определять режим экспорта для каждой ссылки. |
| Inline | `1` | Экспортировать все ссылки как встроенные блоки. |
| Reference | `2` | Экспортировать все ссылки как блоки ссылок. |

## Примеры

Показывает, как ссылки будут записаны в файл .md.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

// Изображение будет записано как ссылка:
// ![ссылка1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// Изображение будет записано как встроенное:
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
