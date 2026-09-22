---
title: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix metodu"
linktitle: "get_IdPrefix"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix metodu. Çıktı belgesindeki tüm oluşturulan öğe kimliklerine (ID) eklenen bir önek belirtir. Varsayılan değer null'dır ve C++'ta hiçbir önek eklenmez."
type: docs
weight: 4250
url: /tr/cpp/aspose.words.saving/svgsaveoptions/get_idprefix/
---
## SvgSaveOptions::get_IdPrefix method


Çıktı belgesindeki tüm oluşturulan öğe kimliklerine (ID) ön ek eklenmesini belirtir. Varsayılan değer null'dır ve hiçbir ön ek eklenmez.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix() const
```


## Örnekler



Tüm oluşturulan öğe kimliklerine (svg) eklenen bir önek nasıl eklenir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

## Ayrıca Bakınız

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
