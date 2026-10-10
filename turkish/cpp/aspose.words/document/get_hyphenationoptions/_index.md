---
title: "Aspose::Words::Document::get_HyphenationOptions method"
linktitle: "get_HyphenationOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_HyphenationOptions yöntemi. C++'ta belge heceleme seçeneklerine erişim sağlar."
type: docs
weight: 32000
url: /tr/cpp/aspose.words/document/get_hyphenationoptions/
---
## Document::get_HyphenationOptions method


Belge heceleme seçeneklerine erişim sağlar.

```cpp
System::SharedPtr<Aspose::Words::Settings::HyphenationOptions> Aspose::Words::Document::get_HyphenationOptions()
```


## Örnekler



Otomatik tirelemeyi nasıl yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## Ayrıca Bakınız

* Class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
