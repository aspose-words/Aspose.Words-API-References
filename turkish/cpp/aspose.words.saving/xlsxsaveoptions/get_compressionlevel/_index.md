---
title: "Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel metodu"
linktitle: "get_CompressionLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel metodu. Belgeyi kaydetmek için kullanılan sıkıştırma seviyesini belirtir. Varsayılan değer C++'ta Normal'dir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/xlsxsaveoptions/get_compressionlevel/
---
## XlsxSaveOptions::get_CompressionLevel method


Belgeyi kaydetmek için kullanılan sıkıştırma seviyesini belirtir. Varsayılan değer [Normal](../../compressionlevel/) dir.

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel() const
```


## Örnekler



XLSX belgesinin nasıl sıkıştırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## Ayrıca Bakınız

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
