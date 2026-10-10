---
title: "Aspose::Words::Drawing::GlowFormat sınıfı"
linktitle: "GlowFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::GlowFormat sınıfı. C++'ta bir nesne için parıltı biçimlendirmesini temsil eder."
type: docs
weight: 1500
url: /tr/cpp/aspose.words.drawing/glowformat/
---
## GlowFormat class


Bir nesne için parıltı biçimlendirmesini temsil eder.

```cpp
class GlowFormat : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Color](./get_color/)() | Parıltı etkisi için rengi temsil eden bir **Color** nesnesini alır veya ayarlar. Varsayılan değer **Black**. |
| [get_Radius](./get_radius/)() | Parıltı etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değerini alır veya ayarlar. Varsayılan değer 0.0. |
| [get_Transparency](./get_transparency/)() | Parıltı etkisi için şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak alır veya ayarlar. Varsayılan değer 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | [GlowFormat](./) öğesini üst nesneden kaldırır. |
| [set_Color](./set_color/)(System::Drawing::Color) | [Aspose::Words::Drawing::GlowFormat::get_Color](./get_color/) için ayarlayıcı. |
| [set_Radius](./set_radius/)(double) | [Aspose::Words::Drawing::GlowFormat::get_Radius](./get_radius/) için ayarlayıcı. |
| [set_Transparency](./set_transparency/)(double) | [Aspose::Words::Drawing::GlowFormat::get_Transparency](./get_transparency/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


[Glow](../shapebase/get_glow/) özelliğini bir nesnenin parıltı özelliklerine erişmek için kullanın. [GlowFormat](./) sınıfının örneklerini doğrudan oluşturmazsınız.

## Örnekler



Parıltı şekil etkisiyle nasıl etkileşim kurulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Glow()->set_Color(System::Drawing::Color::get_Salmon());
shape->get_Glow()->set_Radius(30);
shape->get_Glow()->set_Transparency(0.15);

doc->Save(get_ArtifactsDir() + u"Shape.Glow.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Glow.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::Drawing::Color::FromArgb(217, 250, 128, 114).ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(30, shape->get_Glow()->get_Radius());
ASSERT_NEAR(0.15, shape->get_Glow()->get_Transparency(), 0.01);

shape->get_Glow()->Remove();

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Radius());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Transparency());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
