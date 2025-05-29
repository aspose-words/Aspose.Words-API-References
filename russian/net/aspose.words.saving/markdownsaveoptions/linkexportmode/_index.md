---
title: MarkdownSaveOptions.LinkExportMode
linktitle: LinkExportMode
articleTitle: LinkExportMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MarkdownSaveOptions LinkExportMode для управления форматированием ссылок в выходных файлах. Оптимизируйте экспорт документов без усилий!
type: docs
weight: 100
url: /ru/net/aspose.words.saving/markdownsaveoptions/linkexportmode/
---
## MarkdownSaveOptions.LinkExportMode property

Указывает, как ссылки будут записаны в выходной файл. Значение по умолчанию:Auto .

```csharp
public MarkdownLinkExportMode LinkExportMode { get; set; }
```

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

* enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
