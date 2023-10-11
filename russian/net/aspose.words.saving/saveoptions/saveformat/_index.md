---
title: SaveOptions.SaveFormat
second_title: Справочник по API Aspose.Words для .NET
description: SaveOptions свойство. Указывает формат в котором документ будет сохранен если используется этот объект параметров сохранения.
type: docs
weight: 130
url: /ru/net/aspose.words.saving/saveoptions/saveformat/
---
## SaveOptions.SaveFormat property

Указывает формат, в котором документ будет сохранен, если используется этот объект параметров сохранения.

```csharp
public abstract SaveFormat SaveFormat { get; set; }
```

### Примеры

Показывает, как использовать определенную кодировку при сохранении документа в формате .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Используйте объект SaveOptions, чтобы указать кодировку документа, который мы сохраним.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// По умолчанию выходной документ .epub будет содержать все свое содержимое в одной HTML-части.
// Критерий разделения позволяет нам сегментировать документ на несколько частей HTML.
// Мы установим критерии для разделения документа на абзацы заголовков.
// Это полезно для читателей, которые не могут читать HTML-файлы, размер которых превышает определенный размер.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Указываем, что хотим экспортировать свойства документа.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../saveoptions/)
* сборка [Aspose.Words](../../../)


