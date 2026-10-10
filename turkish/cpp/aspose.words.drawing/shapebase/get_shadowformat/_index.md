---
title: "Aspose::Words::Drawing::ShapeBase::get_ShadowFormat yöntemi"
linktitle: "get_ShadowFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_ShadowFormat yöntemi. Şeklin gölge biçimlendirmesini alır C++'da."
type: docs
weight: 47000
url: /tr/cpp/aspose.words.drawing/shapebase/get_shadowformat/
---
## ShapeBase::get_ShadowFormat method


Şekil için gölge biçimlendirmesini alır.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> Aspose::Words::Drawing::ShapeBase::get_ShadowFormat()
```


## Örnekler



Gölge rengini almayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## Ayrıca Bakınız

* Class [ShadowFormat](../../shadowformat/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
