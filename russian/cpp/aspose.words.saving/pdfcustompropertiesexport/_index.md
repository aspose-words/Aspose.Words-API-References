---
title: "Aspose::Words::Saving::PdfCustomPropertiesExport enum"
linktitle: "PdfCustomPropertiesExport"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfCustomPropertiesExport enum. Указывает способ, которым CustomDocumentProperties экспортируются в PDF‑файл в C++."
type: docs
weight: 74000
url: /ru/cpp/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enum


Указывает способ, которым [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) экспортируются в PDF‑файл.

```cpp
enum class PdfCustomPropertiesExport
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Пользовательские свойства не экспортируются. |
| Стандартный | 1 | Пользовательские свойства экспортируются как записи в словарь /Info. Пользовательские свойства со следующими именами не экспортируются: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped". |
| Метаданные | 2 | Пользовательские свойства являются Метаданными. |

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
