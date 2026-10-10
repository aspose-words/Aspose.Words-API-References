---
title: "Aspose::Words::Document::get_JustificationMode yöntemi"
linktitle: "get_JustificationMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_JustificationMode yöntemi. C++'ta bir belgenin karakter aralığı ayarlamasını alır veya ayarlar."
type: docs
weight: 34000
url: /tr/cpp/aspose.words/document/get_justificationmode/
---
## Document::get_JustificationMode method


Belgenin karakter aralığı ayarlamasını alır veya ayarlar.

```cpp
Aspose::Words::Settings::JustificationMode Aspose::Words::Document::get_JustificationMode()
```


## Örnekler



Karakter aralığı kontrolünü nasıl yöneteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## Ayrıca Bakınız

* Enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
