---
title: Aspose::Words::Saving::XlsxSaveOptions::set_DateTimeParsingMode method
linktitle: set_DateTimeParsingMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XlsxSaveOptions::set_DateTimeParsingMode method. Sets the mode that specifies how document text is parsed to identify date and time values. The default value is UseCurrentLocale in C++.'
type: docs
weight: 7500
url: /cpp/aspose.words.saving/xlsxsaveoptions/set_datetimeparsingmode/
---
## XlsxSaveOptions::set_DateTimeParsingMode method


Sets the mode that specifies how document text is parsed to identify date and time values. The default value is [UseCurrentLocale](../../xlsxdatetimeparsingmode/).

```cpp
void Aspose::Words::Saving::XlsxSaveOptions::set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode value)
```

## Examples


Shows how to specify autodetection of the date time format.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Xlsx DateTime.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// Specify using datetime format autodetection.
saveOptions->set_DateTimeParsingMode(XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```
## See Also

* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
