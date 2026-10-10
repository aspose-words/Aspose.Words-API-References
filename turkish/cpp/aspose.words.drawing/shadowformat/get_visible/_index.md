---
title: "Aspose::Words::Drawing::ShadowFormat::get_Visible metodu"
linktitle: "get_Visible"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShadowFormat::get_Visible metodu. Bu örneğe uygulanan biçimlendirme C++'ta görünürse true döndürür."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.drawing/shadowformat/get_visible/
---
## ShadowFormat::get_Visible method


Bu örneğe uygulanan biçimlendirme görünürse **true** döndürür.

```cpp
bool Aspose::Words::Drawing::ShadowFormat::get_Visible()
```


## Örnekler



Bir şekil için gölge biçimlendirmesiyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## Ayrıca Bakınız

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
