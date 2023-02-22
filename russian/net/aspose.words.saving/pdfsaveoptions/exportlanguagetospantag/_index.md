---
title: PdfSaveOptions.ExportLanguageToSpanTag
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Получает или задает значение определяющее следует ли создавать тег Span в структуре документа для экспорта языка текста.
type: docs
weight: 130
url: /ru/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Получает или задает значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта языка текста.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

### Примечания

Значение по умолчанию`ЛОЖЬ` а атрибут «Lang» прикрепляется к последовательности отмеченного содержимого в потоке содержимого страницы.

Когда значение`истинный` Тег "Span" создается для текста с нестандартным языком и к этому тегу прикрепляется атрибут "Lang".

Это значение игнорируется, когда[`ExportDocumentStructure`](../exportdocumentstructure/) является`ЛОЖЬ` .

### Примеры

Показывает, как создать тег «Span» в структуре документа для экспорта языка текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Обратите внимание: когда «ExportDocumentStructure» имеет значение false, «ExportLanguageToSpanTag» игнорируется.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


