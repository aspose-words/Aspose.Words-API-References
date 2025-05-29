---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ExportLanguageToSpanTag в PdfSaveOptions. Управляйте экспортом языка текста с помощью тегов Span для улучшения структуры документа и доступности.
type: docs
weight: 150
url: /ru/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Возвращает или задает значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта языка текста.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`Атрибут «Lang» прикрепляется к последовательности маркированного содержимого в потоке содержимого страницы.

Когда значение равно`истинный` Тег «Span» создается для текста с нестандартным языком language , и к этому тегу присоединяется атрибут «Lang».

Это значение игнорируется, когда[`ExportDocumentStructure`](../exportdocumentstructure/) является`ЛОЖЬ` .

## Примеры

Показывает, как создать тег «Span» в структуре документа для экспорта языка текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Обратите внимание: если "ExportDocumentStructure" имеет значение false, "ExportLanguageToSpanTag" игнорируется.
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
