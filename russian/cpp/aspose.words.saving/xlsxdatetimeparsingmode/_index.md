---
title: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum. Указывает, как текст документа анализируется для определения значений даты и времени в C++."
type: docs
weight: 86500
url: /ru/cpp/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enum


Указывает, как текст документа анализируется для определения значений даты и времени.

```cpp
enum class XlsxDateTimeParsingMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| UseCurrentLocale | 0 | Сначала используется формат даты и времени, установленный для текущего потока, чтобы разобрать строковые значения. Если разбор не удался, пробуются другие распространённые форматы даты и времени. |
| Авто | 1 | Формат даты и времени, используемый в документе, определяется автоматически. Это может занять дополнительное время. |


## Примеры



Показывает, как указать автоматическое определение формата даты и времени.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// Укажите использование автоматического определения формата даты и времени.
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
