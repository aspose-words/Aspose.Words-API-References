---
title: Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode method
linktitle: get_DateTimeParsingMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode method. Gets or sets the mode that specifies how document text is parsed to identify date and time values. The default value is UseCurrentLocale in C++.'
type: docs
weight: 3500
url: /cpp/aspose.words.saving/xlsxsaveoptions/get_datetimeparsingmode/
---
## XlsxSaveOptions::get_DateTimeParsingMode method


Gets or sets the mode that specifies how document text is parsed to identify date and time values. The default value is [UseCurrentLocale](../../xlsxdatetimeparsingmode/).

```cpp
Aspose::Words::Saving::XlsxDateTimeParsingMode Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode() const
```


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

* Enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
