---
title: HtmlSaveOptions.ExportDocumentProperties
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает экспортировать ли встроенные и настраиваемые свойства документа в HTML MHTML или EPUB. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 130
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportdocumentproperties/
---
## HtmlSaveOptions.ExportDocumentProperties property

Указывает, экспортировать ли встроенные и настраиваемые свойства документа в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportDocumentProperties { get; set; }
```

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

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


