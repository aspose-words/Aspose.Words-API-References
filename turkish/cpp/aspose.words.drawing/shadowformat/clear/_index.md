---
title: "Aspose::Words::Drawing::ShadowFormat::Clear metodu"
linktitle: "Clear"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShadowFormat::Clear metodu. C++'ta gölge biçimini temizler."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat::Clear method


Gölge biçimini temizler.

```cpp
void Aspose::Words::Drawing::ShadowFormat::Clear()
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
