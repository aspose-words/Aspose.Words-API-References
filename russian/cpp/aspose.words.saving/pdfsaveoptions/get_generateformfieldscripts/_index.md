---
title: "метод Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts"
linktitle: "get_GenerateFormFieldScripts"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts. Указывает, следует ли генерировать скрипты, имитирующие определённое поведение полей формы Microsoft Word в PDF. По умолчанию значение false в C++."
type: docs
weight: 18500
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/get_generateformfieldscripts/
---
## PdfSaveOptions::get_GenerateFormFieldScripts method


Указывает, генерировать ли скрипты, имитирующие поведение определённых полей формы Microsoft Word в PDF. По умолчанию **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts() const
```

## Примечания


Когда эта опция включена, экспортёр генерирует действия PDF JavaScript для имитации поведения полей формы Microsoft Word, таких как поля даты и времени с форматированием и правилами проверки.

Когда установлено в **true**, поддерживаемое поведение будет экспортировано как действия PDF JavaScript. Когда установлено в **false**, скрипты полей формы генерироваться не будут.

Выполнение скриптов зависит от PDF‑просмотрщика. Некоторые PDF‑просмотрщики могут игнорировать скрипты, ограничивать их выполнение или требовать от пользователя включить JavaScript.

Действия JavaScript запрещены в соответствии с PDF/A-1, PDF/A-2 и PDF/A-3. Значение **false** будет использовано автоматически в этом случае.
## См. также

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
