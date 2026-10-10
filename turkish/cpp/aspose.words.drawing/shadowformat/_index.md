---
title: "Aspose::Words::Drawing::ShadowFormat class"
linktitle: "ShadowFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShadowFormat class. Bir nesne için gölge biçimlendirmesini temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.drawing/shadowformat/
---
## ShadowFormat class


Bir nesne için gölge biçimlendirmesini temsil eder. Daha fazla bilgi edinmek için [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/) dokümantasyon makalesini ziyaret edin.

```cpp
class ShadowFormat : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clear](./clear/)() | Gölge biçimini temizler. |
| [get_Color](./get_color/)() | Gölge rengi temsil eden bir **Color** nesnesini alır veya ayarlar. Varsayılan değer **Black**'dır. |
| [get_Transparency](./get_transparency/)() | Gölge etkisi için şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak alır veya ayarlar. Varsayılan değer 0.0'dır. |
| [get_Type](./get_type/)() | Belirtilen [ShadowType](../shadowtype/) öğesini [ShadowFormat](./) için alır veya ayarlar. |
| [get_Visible](./get_visible/)() | Bu örneğe uygulanan biçimlendirme görünürse **true** döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | [Aspose::Words::Drawing::ShadowFormat::get_Color](./get_color/) için ayarlayıcı. |
| [set_Transparency](./set_transparency/)(double) | [Aspose::Words::Drawing::ShadowFormat::get_Transparency](./get_transparency/) için ayarlayıcı. |
| [set_Type](./set_type/)(Aspose::Words::Drawing::ShadowType) | [Aspose::Words::Drawing::ShadowFormat::get_Type](./get_type/) için ayarlayıcı. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
