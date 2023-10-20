---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words для .NET
description: HtmlSaveOptions DocumentSplitCriteria свойство. Указывает как документ должен быть разделен при сохранении вHtml  Epub илиAzw3 формат. По умолчаниюNone для HTML и HeadingParagraph для EPUB и AZW3 на С#.
type: docs
weight: 80
url: /ru/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Указывает, как документ должен быть разделен при сохранении вHtml , Epub илиAzw3 формат. По умолчаниюNone для HTML и HeadingParagraph для EPUB и AZW3.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## Примечания

Обычно вам нужно сохранить документ в HTML как один файл. Но в некоторых случаях предпочтительнее разделить вывод на несколько небольших HTML-страниц. При сохранении в формате HTML эти страницы будут выводиться в отдельные файлы или потоки. При сохранении в формате EPUB они будут включены в соответствующие пакеты.

Документ невозможно разделить при сохранении в формате MHTML.

## Примеры

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
