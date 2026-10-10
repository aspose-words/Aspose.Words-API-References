---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode metod"
linktitle: "get_DateTimeParsingMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode metod. Hämtar eller anger läget som specificerar hur dokumenttexten analyseras för att identifiera datum- och tidsvärden. Standardvärdet är UseCurrentLocale i C++."
type: docs
weight: 3500
url: /sv/cpp/aspose.words.saving/xlsxsaveoptions/get_datetimeparsingmode/
---
## XlsxSaveOptions::get_DateTimeParsingMode method


Hämtar eller anger läget som specificerar hur dokumenttexten analyseras för att identifiera datum- och tidsvärden. Standardvärdet är [UseCurrentLocale](../../xlsxdatetimeparsingmode/).

```cpp
Aspose::Words::Saving::XlsxDateTimeParsingMode Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode() const
```


## Exempel



Visar hur man specificerar automatisk upptäckt av datum- och tidsformatet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// Ange att använda automatisk upptäckt av datum- och tidsformat.
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## Se även

* Enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
