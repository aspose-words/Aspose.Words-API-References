---
title: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData method"
linktitle: "get_IgnoreOleData"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData yöntemi. C++'da OLE verisinin göz ardı edilip edilmeyeceğini belirtir."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.loading/loadoptions/get_ignoreoledata/
---
## LoadOptions::get_IgnoreOleData method


OLE verisinin ihmal edilip edilmeyeceğini belirtir.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_IgnoreOleData() const
```

## Açıklamalar


OLE verisini göz ardı etmek, hedef format OLE nesnelerini desteklemediğinde veri kaybı olmadan bellek tüketimini azaltabilir ve performansı artırabilir.

Varsayılan değer **false**'tur.

## Örnekler



Yükleme sırasında OLE verisinin nasıl göz ardı edileceğini gösterir.
```cpp
// OLE verisini göz ardı etmek, bellek tüketimini azaltabilir ve performansı artırabilir
// hedef format OLE nesnelerini desteklemediğinde veri kaybı olmadan.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_IgnoreOleData(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.IgnoreOleData.docx");
```

## Ayrıca Bakınız

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
