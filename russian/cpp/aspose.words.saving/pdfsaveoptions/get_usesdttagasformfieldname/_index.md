---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName метод"
linktitle: "get_UseSdtTagAsFormFieldName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName метод. Указывает, использовать ли свойство Tag или Id элемента управления SDT в качестве имени поля формы в PDF в C++."
type: docs
weight: 32500
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_usesdttagasformfieldname/
---
## PdfSaveOptions::get_UseSdtTagAsFormFieldName method


Указывает, следует ли использовать свойство Tag или Id элемента управления SDT в качестве имени поля формы в PDF.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName() const
```

## Примечания


Значение по умолчанию — **false**.

Когда установлено в **false**, свойство Id элемента управления SDT используется в качестве имени поля формы в PDF.

Когда установлено в **true**, свойство Tag элемента управления SDT используется в качестве имени поля формы в PDF.

Если установлено в **true** и Tag пустой, будет использовано свойство Id в качестве имени поля формы.

Если установлено в **true** и значения Tag не уникальны, дублирующиеся значения Tag будут изменены для создания уникальных имён полей формы PDF.
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
