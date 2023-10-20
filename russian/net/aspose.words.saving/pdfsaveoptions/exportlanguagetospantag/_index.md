---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words для .NET
description: PdfSaveOptions ExportLanguageToSpanTag свойство. Получает или задает значение определяющее следует ли создавать тег Span в структуре документа для экспорта текстового языка на С#.
type: docs
weight: 150
url: /ru/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Получает или задает значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта текстового языка.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`а атрибут «Lang» прикрепляется к последовательности маркированного контента в потоке контента страницы.

Когда значение`истинный` Тег «Span» создается для текста с языком не по умолчанию , и к этому тегу прикреплен атрибут «Lang».

Это значение игнорируется, если[`ExportDocumentStructure`](../exportdocumentstructure/) является`ЛОЖЬ` .

## Примеры

Показывает, как создать тег «Span» в структуре документа для экспорта языка текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Обратите внимание: если «ExportDocumentStructure» имеет значение false, «ExportLanguageToSpanTag» игнорируется.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
