---
title: "Aspose::Words::Settings::JustificationMode enum"
linktitle: "JustificationMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::JustificationMode enum. Bir belge için karakter aralığı ayarlamasını belirtir. Varsayılan değer C++'da Expand'tir."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.settings/justificationmode/
---
## JustificationMode enum


Bir belge için karakter aralığı ayarlamasını belirtir. Varsayılan değer **Expand**.

```cpp
enum class JustificationMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Expand | 0 | Karakter aralığını sıkıştırma. |
| Compress | 1 | Karakter aralığını sıkıştır. |
| CompressKana | 2 | Kana hece sistemlerinin kurallarını kullanarak, Hiragana ve Katakana ile sıkıştır. |


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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
