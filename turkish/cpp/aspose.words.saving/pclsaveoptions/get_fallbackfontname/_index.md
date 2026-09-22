---
title: "Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName yöntemi"
linktitle: "get_FallbackFontName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName yöntemi. Yazıcıda ve yerleşik yazı tipi koleksiyonlarında beklenen bir yazı tipi bulunamazsa kullanılacak yazı tipinin adını döndürür."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/pclsaveoptions/get_fallbackfontname/
---
## PclSaveOptions::get_FallbackFontName method


Yazıcıda ve yerleşik yazı tipi koleksiyonlarında beklenen bir yazı tipi bulunamazsa kullanılacak yazı tipinin adı.

```cpp
System::String Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName() const
```


## Örnekler



Orijinal yazı tipi mevcut olmadığında, yazıcının basılmış metne bir yedek olarak uygulayacağı bir yazı tipinin nasıl bildirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_FallbackFontName(u"Times New Roman");

// Bu belge, eksik yazı tipine sahip metne "Times New Roman" uygulanması için yazıcıyı yönlendirecektir.
// "Times New Roman" da mevcut değilse, yazıcı varsayılan olarak "Arial" yazı tipini kullanacaktır.
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

## Ayrıca Bakınız

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
