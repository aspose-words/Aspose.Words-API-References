---
title: "Метод Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields"
linktitle: "get_PreserveFormFields"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields. Указывает, следует ли сохранять поля формы Microsoft Word как поля формы в PDF или преобразовывать их в текст. По умолчанию false в C++."
type: docs
weight: 28000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_preserveformfields/
---
## PdfSaveOptions::get_PreserveFormFields method


Указывает, следует ли сохранять поля формы Microsoft Word как поля формы в PDF или преобразовывать их в текст. По умолчанию **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields() const
```

## Примечания


Поля формы Microsoft Word включают элементы ввода текста, выпадающие списки и флажки.

Когда установлено значение **false**, эти поля будут экспортированы в PDF как текст. Когда установлено значение **true**, эти поля будут экспортированы в PDF как поля формы.

При экспорте полей формы в PDF как полей формы может произойти частичная потеря форматирования, поскольку поля формы PDF не поддерживают все возможности полей формы Microsoft Word.

Кроме того, размер выходного файла зависит от размера содержимого, поскольку редактируемые формы в Microsoft Word являются встроенными объектами.
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
