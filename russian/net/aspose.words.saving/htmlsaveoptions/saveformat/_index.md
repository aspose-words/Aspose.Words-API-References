---
title: HtmlSaveOptions.SaveFormat
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает формат в котором документ будет сохранен если используется этот объект параметров сохранения. Может бытьHtml Mhtml Epub  Azw3 илиMobi .
type: docs
weight: 440
url: /ru/net/aspose.words.saving/htmlsaveoptions/saveformat/
---
## HtmlSaveOptions.SaveFormat property

Указывает формат, в котором документ будет сохранен, если используется этот объект параметров сохранения. Может бытьHtml ,Mhtml ,Epub , Azw3 илиMobi .

```csharp
public override SaveFormat SaveFormat { get; set; }
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
* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


