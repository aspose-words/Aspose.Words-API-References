---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlSaveOptions DocumentSplitCriteria для оптимизации сохранения документов в форматах HTML, EPUB и AZW3. Расширьте контроль над форматированием уже сегодня!
type: docs
weight: 80
url: /ru/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Указывает, как следует разделить документ при сохранении вHtml , Epub илиAzw3 format. Значение по умолчанию:None для HTML и HeadingParagraph для EPUB и AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## Примечания

Обычно документ сохраняется в формате HTML как один файл. Но в некоторых случаях предпочтительнее разделить вывод на несколько страниц HTML меньшего размера. При сохранении в формате HTML эти страницы будут выводиться в отдельные файлы или потоки. При сохранении в формате EPUB они будут включены в соответствующие пакеты.

Документ невозможно разделить при сохранении в формате MHTML.

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
