---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode metodu"
linktitle: "get_SectionMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode yöntemi. Çıktı XLSX belgesine kaydedilirken bölümlerin nasıl işlendiğini alır veya ayarlar. Varsayılan değer C++'da MultipleWorksheets'tir."
type: docs
weight: 4500
url: /tr/cpp/aspose.words.saving/xlsxsaveoptions/get_sectionmode/
---
## XlsxSaveOptions::get_SectionMode method


Çıktı XLSX belgesine kaydedilirken bölümlerin nasıl işlendiğini alır veya ayarlar. Varsayılan değer [MultipleWorksheets](../../xlsxsectionmode/).

```cpp
Aspose::Words::Saving::XlsxSectionMode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode() const
```


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

* Enum [XlsxSectionMode](../../xlsxsectionmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
