---
title: "метод Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag"
linktitle: "get_ExportLanguageToSpanTag"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag. Получает или задает значение, определяющее, следует ли создавать тег \\\"Span\\\" в структуре документа для экспорта языка текста в C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_exportlanguagetospantag/
---
## PdfSaveOptions::get_ExportLanguageToSpanTag method


Получает или задаёт значение, определяющее, создавать ли тег "Span" в структуре документа для экспорта языка текста.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag() const
```

## Примечания


Значение по умолчанию — **false**, и атрибут \"Lang\" присоединяется к последовательности отмеченного содержимого в потоке содержимого страницы.

Когда значение **true**, тег \"Span\" создаётся для текста с нестандартным языком, и атрибут \"Lang\" присоединяется к этому тегу.

Это значение игнорируется, когда [ExportDocumentStructure](../get_exportdocumentstructure/) равно **false**.
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
