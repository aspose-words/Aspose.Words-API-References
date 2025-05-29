---
title: HtmlSaveOptions.ExportDocumentProperties
linktitle: ExportDocumentProperties
articleTitle: ExportDocumentProperties
second_title: Aspose.Words для .NET
description: Узнайте, как ExportDocumentProperties из HtmlSaveOptions улучшает экспорт HTML, MHTML или EPUB, включая основные встроенные и пользовательские свойства документа.
type: docs
weight: 120
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportdocumentproperties/
---
## HtmlSaveOptions.ExportDocumentProperties property

Указывает, следует ли экспортировать встроенные и пользовательские свойства документа в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportDocumentProperties { get; set; }
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

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
