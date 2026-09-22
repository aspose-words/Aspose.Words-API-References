---
title: "Aspose::Words::Saving::XlsxSectionMode enum"
linktitle: "XlsxSectionMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XlsxSectionMode enum. Bir belge XLSX formatında C++ ile kaydedilirken bölümlerin nasıl işlendiğini belirtir."
type: docs
weight: 87000
url: /tr/cpp/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enum


Bir belge XLSX formatında kaydedilirken bölümlerin nasıl işlendiğini belirtir.

```cpp
enum class XlsxSectionMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| MultipleWorksheets | 0 | Bir belgenin her bölümü için ayrı bir çalışma sayfası oluşturulduğunu belirtir. |
| SingleWorksheet | 1 | Bir belgenin tüm bölümlerinin tek bir çalışma sayfasına kaydedildiğini belirtir. |


## Örnekler



Belgeyi ayrı çalışma sayfaları olarak kaydetmenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Bir belgenin her bölümü ayrı bir çalışma sayfası olarak oluşturulacaktır.
// 'SingleWorksheet' kullanarak tüm belgeyi tek bir çalışma sayfasında görüntüleyin.
auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_SectionMode(Aspose::Words::Saving::XlsxSectionMode::MultipleWorksheets);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
