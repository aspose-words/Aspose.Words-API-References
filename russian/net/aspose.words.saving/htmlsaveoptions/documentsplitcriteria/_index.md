---
title: HtmlSaveOptions.DocumentSplitCriteria
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает как документ должен быть разделен при сохранении вHtml илиEpub формат. По умолчаниюNone для HTML и HeadingParagraph для EPUB.
type: docs
weight: 80
url: /ru/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Указывает, как документ должен быть разделен при сохранении вHtml илиEpub формат. По умолчаниюNone для HTML и HeadingParagraph для EPUB.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

### Примечания

Обычно вы хотите, чтобы документ был сохранен в HTML как один файл. Но в некоторых случаях предпочтительнее разбить вывод на несколько меньших HTML-страниц. При сохранении в формате HTML эти страницы будут выводиться в отдельные файлы или потоки. При сохранении в формате EPUB они будут включены в соответствующие пакеты.

Документ нельзя разделить при сохранении в формате MHTML.

### Примеры

Показывает, как использовать определенную кодировку при сохранении документа в формате .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Используйте объект SaveOptions для указания кодировки сохраняемого документа.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// По умолчанию выходной документ .epub будет иметь все свое содержимое в одной HTML-части.
// Критерий разделения позволяет нам разделить документ на несколько частей HTML.
// Мы установим критерии для разделения документа на абзацы заголовков.
// Это полезно для читателей, которые не могут читать файлы HTML, размер которых превышает определенный.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Указываем, что хотим экспортировать свойства документа.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Смотрите также

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


