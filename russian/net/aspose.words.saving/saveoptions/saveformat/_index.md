---
title: SaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство SaveOptions SaveFormat, чтобы легко выбирать формат сохранения документа для оптимальной гибкости и контроля.
type: docs
weight: 130
url: /ru/net/aspose.words.saving/saveoptions/saveformat/
---
## SaveOptions.SaveFormat property

Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения.

```csharp
public abstract SaveFormat SaveFormat { get; set; }
```

## Примеры

Показывает, как использовать определенную кодировку при сохранении документа в формате .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Используйте объект SaveOptions, чтобы указать кодировку документа, который мы будем сохранять.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// По умолчанию выходной документ .epub будет иметь все свое содержимое в одной части HTML.
// Критерий разделения позволяет нам сегментировать документ на несколько частей HTML.
// Мы установим критерии для разделения документа на заголовочные абзацы.
// Это полезно для читателей, которые не могут читать HTML-файлы, размер которых больше определенного значения.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Указываем, что мы хотим экспортировать свойства документа.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
