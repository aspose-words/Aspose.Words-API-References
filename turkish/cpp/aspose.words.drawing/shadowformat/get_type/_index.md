---
title: "Aspose::Words::Drawing::ShadowFormat::get_Type metodu"
linktitle: "get_Type"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShadowFormat::get_Type metodu. C++'ta ShadowFormat için belirtilen ShadowType'ı alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing/shadowformat/get_type/
---
## ShadowFormat::get_Type method


Belirtilen [ShadowType](../../shadowtype/) için [ShadowFormat](../) alır veya ayarlar.

```cpp
Aspose::Words::Drawing::ShadowType Aspose::Words::Drawing::ShadowFormat::get_Type()
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

* Enum [ShadowType](../../shadowtype/)
* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
