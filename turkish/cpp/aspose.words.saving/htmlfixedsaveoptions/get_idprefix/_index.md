---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix yöntemi"
linktitle: "get_IdPrefix"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix yöntemi. Çıktı belgesindeki tüm oluşturulan öğe kimliklerine ön ek ekleyen bir önek belirtir. Varsayılan değer null'dur ve C++'ta hiçbir önek eklenmez."
type: docs
weight: 10500
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_idprefix/
---
## HtmlFixedSaveOptions::get_IdPrefix method


Çıktı belgesindeki tüm oluşturulan öğe kimliklerine (ID) ön ek eklenmesini belirtir. Varsayılan değer null'dır ve hiçbir ön ek eklenmez.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix() const
```


## Örnekler



Tüm oluşturulan öğe kimliklerine ön ek eklemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

## Ayrıca Bakınız

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
