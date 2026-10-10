---
title: "Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine yöntemi"
linktitle: "get_MaxCharactersPerLine"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine yöntemi. Bir satır başına maksimum karakter sayısını belirten bir tamsayı değerini alır veya ayarlar. Varsayılan değer 0'dır, bu C++'ta sınırsız anlamına gelir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/txtsaveoptions/get_maxcharactersperline/
---
## TxtSaveOptions::get_MaxCharactersPerLine method


Bir satır başına maksimum karakter sayısını belirten bir tamsayı değerini alır veya ayarlar. Varsayılan değer 0'dır, bu da sınırsız anlamına gelir.

```cpp
int32_t Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine() const
```


## Örnekler



Satır başına maksimum karakter sayısını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Bir satırda izin verilen maksimum 30 karakteri ayarlayın.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_MaxCharactersPerLine(30);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

## Ayrıca Bakınız

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
