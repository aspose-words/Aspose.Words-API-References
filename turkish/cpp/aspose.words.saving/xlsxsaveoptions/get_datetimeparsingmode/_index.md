---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode yöntemi"
linktitle: "get_DateTimeParsingMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode yöntemi. Belge metninin tarih ve saat değerlerini tanımlamak için nasıl ayrıştırıldığını belirten modu alır veya ayarlar. Varsayılan değer C++'da UseCurrentLocale'tir."
type: docs
weight: 3500
url: /tr/cpp/aspose.words.saving/xlsxsaveoptions/get_datetimeparsingmode/
---
## XlsxSaveOptions::get_DateTimeParsingMode method


Belge metninin tarih ve saat değerlerini tanımlamak için nasıl ayrıştırıldığını belirten modu alır veya ayarlar. Varsayılan değer [UseCurrentLocale](../../xlsxdatetimeparsingmode/).

```cpp
Aspose::Words::Saving::XlsxDateTimeParsingMode Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode() const
```


## Örnekler



Tarih‑saat biçiminin otomatik algılanmasını nasıl belirteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Xlsx DateTime.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
// Tarih‑saat biçimi otomatik algılamasını belirtin.
saveOptions->set_DateTimeParsingMode(Aspose::Words::Saving::XlsxDateTimeParsingMode::Auto);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

## Ayrıca Bakınız

* Enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
