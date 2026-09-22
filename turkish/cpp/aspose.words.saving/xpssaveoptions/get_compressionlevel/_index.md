---
title: "Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel yöntemi"
linktitle: "get_CompressionLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel yöntemi. Belgeyi kaydetmek için kullanılan sıkıştırma seviyesini belirtir. Varsayılan değer C++'ta Normal'dir."
type: docs
weight: 2250
url: /tr/cpp/aspose.words.saving/xpssaveoptions/get_compressionlevel/
---
## XpsSaveOptions::get_CompressionLevel method


Belgeyi kaydetmek için kullanılan sıkıştırma seviyesini belirtir. Varsayılan değer [Normal](../../compressionlevel/) dir.

```cpp
Aspose::Words::Saving::CompressionLevel Aspose::Words::Saving::XpsSaveOptions::get_CompressionLevel() const
```


## Örnekler



Bir belgeyi XPS formatında kaydederken sıkıştırma seviyesini nasıl kontrol edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample document for XPS compression test.");

// Bir XpsSaveOptions nesnesi oluşturun ve sıkıştırma seviyesini ayarlayın.
auto options = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();
options->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.CompressionLevelXps.xps", options);
```

## Ayrıca Bakınız

* Enum [CompressionLevel](../../compressionlevel/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
