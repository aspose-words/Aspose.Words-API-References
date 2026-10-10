---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont yöntemi"
linktitle: "get_UpdateAmbiguousTextFont"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont yöntemi. Kullanılan karakter koduna göre yazı tipi özelliklerinin değişip değişmeyeceğini belirler (C++)."
type: docs
weight: 15500
url: /tr/cpp/aspose.words.saving/saveoptions/get_updateambiguoustextfont/
---
## SaveOptions::get_UpdateAmbiguousTextFont method


Yazı tipi özniteliklerinin kullanılan karakter koduna göre değiştirilip değiştirilmeyeceğini belirler.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont() const
```


## Örnekler



Kullanılan karakter koduna uygun olarak yazı tipini nasıl güncelleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Special symbol.docx");
System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
std::cout << run->get_Text() << std::endl;
// ฿
std::cout << run->get_Font()->get_Name() << std::endl;
// Arial

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateAmbiguousTextFont(true);
doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
std::cout << run->get_Text() << std::endl;
// ฿
std::cout << run->get_Font()->get_Name() << std::endl;
// Angsana New
```

## Ayrıca Bakınız

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
