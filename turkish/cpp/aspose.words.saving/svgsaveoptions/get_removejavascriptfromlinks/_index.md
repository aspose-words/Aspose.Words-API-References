---
title: "Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks yöntemi"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks yöntemi. Bağlantılardan JavaScript'in kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer false'tur. Bu seçenek etkinleştirildiğinde, JavaScript içeren tüm bağlantılar C++'ta \"javascript:void(0)\" ile değiştirilir."
type: docs
weight: 4750
url: /tr/cpp/aspose.words.saving/svgsaveoptions/get_removejavascriptfromlinks/
---
## SvgSaveOptions::get_RemoveJavaScriptFromLinks method


Bağlantılardan JavaScript'in kaldırılıp kaldırılmayacağını belirtir. Varsayılan **false**'dur. Bu seçenek etkinleştirildiğinde, JavaScript içeren tüm bağlantılar "javascript:void(0)" ile değiştirilir.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Örnekler



Bağlantılardan (svg) JavaScript'in nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

## Ayrıca Bakınız

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
