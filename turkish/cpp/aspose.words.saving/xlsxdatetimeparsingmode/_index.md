---
title: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum"
linktitle: "XlsxDateTimeParsingMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XlsxDateTimeParsingMode enum. Belge metninin C++'de tarih ve saat değerlerini tanımlamak için nasıl ayrıştırıldığını belirtir."
type: docs
weight: 86500
url: /tr/cpp/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enum


Belge metninin tarih ve saat değerlerini tanımlamak için nasıl ayrıştırıldığını belirtir.

```cpp
enum class XlsxDateTimeParsingMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| UseCurrentLocale | 0 | Geçerli iş parçacığı için ayarlanan tarih‑saat biçimi, önce dize değerlerini ayrıştırmak için kullanılır. Ayrıştırma başarısız olursa, diğer yaygın tarih‑saat biçimleri denenir. |
| Otomatik | 1 | Bir belgede kullanılan tarih‑saat biçimi otomatik olarak belirlenir. Bu ek zaman alabilir. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
