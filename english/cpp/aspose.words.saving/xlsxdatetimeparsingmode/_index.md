---
title: Aspose::Words::Saving::XlsxDateTimeParsingMode enum
linktitle: XlsxDateTimeParsingMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XlsxDateTimeParsingMode enum. Specifies how document text is parsed to identify date and time values in C++.'
type: docs
weight: 86500
url: /cpp/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enum


Specifies how document text is parsed to identify date and time values.

```cpp
enum class XlsxDateTimeParsingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| UseCurrentLocale | 0 | The datetime format set for the current thread is used first to parse string values. If the parsing fails, other common datetime formats are tried. |
| Auto | 1 | The datetime format used in a document is determined automatically. This may take additional time. |


## Examples



Shows how to specify autodetection of the date time format. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// Specify using datetime format autodetection.
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
