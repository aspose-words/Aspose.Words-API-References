---
title: MarkdownSaveOptions.ExportUnderlineFormatting
linktitle: ExportUnderlineFormatting
articleTitle: ExportUnderlineFormatting
second_title: Aspose.Words для .NET
description: Узнайте, как свойство MarkdownSaveOptions ExportUnderlineFormatting улучшает экспорт текста. Легко управляйте форматированием подчеркивания с помощью этой логической настройки.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/markdownsaveoptions/exportunderlineformatting/
---
## MarkdownSaveOptions.ExportUnderlineFormatting property

Возвращает или задает логическое значение, указывающее, следует ли экспортировать подчеркивание форматирования текста как последовательность из двух символов плюс «++». Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportUnderlineFormatting { get; set; }
```

## Примеры

Показывает, как экспортировать подчеркивание в формате ++.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Single;
builder.Write("Lorem ipsum. Dolor sit amet.");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

### Смотрите также

* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
