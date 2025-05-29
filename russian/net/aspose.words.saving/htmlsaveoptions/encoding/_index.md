---
title: HtmlSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words для .NET
description: Откройте для себя кодировку HtmlSaveOptions для бесшовного экспорта HTML, MHTML и EPUB. Легко настройте кодировку с помощью UTF-8 для оптимальной совместимости и производительности.
type: docs
weight: 100
url: /ru/net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

Указывает кодировку, используемую при экспорте в HTML, MHTML или EPUB. Значение по умолчанию:`новая кодировка UTF8(false)` (UTF-8 без BOM).

```csharp
public Encoding Encoding { get; set; }
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
