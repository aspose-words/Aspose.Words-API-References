---
title: "Метод Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode"
linktitle: "get_DateTimeParsingMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode. Получает или задает режим, определяющий, как текст документа анализируется для выявления значений даты и времени. Значение по умолчанию — UseCurrentLocale в C++."
type: docs
weight: 3500
url: /ru/cpp/aspose.words.saving/xlsxsaveoptions/get_datetimeparsingmode/
---
## XlsxSaveOptions::get_DateTimeParsingMode method


Получает или задает режим, определяющий, как текст документа анализируется для выявления значений даты и времени. Значение по умолчанию — [UseCurrentLocale](../../xlsxdatetimeparsingmode/).

```cpp
Aspose::Words::Saving::XlsxDateTimeParsingMode Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode() const
```


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

* Enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
