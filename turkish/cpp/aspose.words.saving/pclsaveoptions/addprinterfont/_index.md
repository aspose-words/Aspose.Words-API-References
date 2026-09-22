---
title: "Aspose::Words::Saving::PclSaveOptions::AddPrinterFont yöntemi"
linktitle: "AddPrinterFont"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PclSaveOptions::AddPrinterFont yöntemi. Üretici tarafından yazıcıya yüklenen yazı tipi hakkında bilgi ekler C++'ta."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions::AddPrinterFont method


Üretici tarafından yazıcıya yüklenen yazı tipi hakkında bilgi ekler.

```cpp
void Aspose::Words::Saving::PclSaveOptions::AddPrinterFont(const System::String &fontFullName, const System::String &fontPclName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontFullName | const System::String\& | Yazı tipinin tam adı (ör. "Times New Roman Bold Italic"). |
| fontPclName | const System::String\& | Pcl belgesinde kullanılan yazı tipinin adı. |

## Örnekler



Belirli bir yazı tipinin tüm örneklerini farklı bir yazı tipiyle değiştirecek şekilde bir yazıcıyı nasıl yapılandırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Courier");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->AddPrinterFont(u"Courier New", u"Courier");

// Bu belgeyi yazdırırken, yazıcı "Courier New" yazı tipini kullanacaktır
// "Courier" yazı tipinin kullanıldığı yerlere erişmek için.
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

## Ayrıca Bakınız

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
