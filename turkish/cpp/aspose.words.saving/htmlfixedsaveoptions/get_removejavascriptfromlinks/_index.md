---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks metodu"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks metodu. Bağlantılardan JavaScript'in kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer C++'da false'tur."
type: docs
weight: 13500
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_removejavascriptfromlinks/
---
## HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks method


Bağlantılardan JavaScript'in kaldırılıp kaldırılmayacağını belirtir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## Örnekler



HTML sabit belgelerindeki bağlantılardan JavaScript'in nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```


Bağlantılardan JavaScript'in nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

## Ayrıca Bakınız

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
