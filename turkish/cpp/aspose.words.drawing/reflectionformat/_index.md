---
title: "Aspose::Words::Drawing::ReflectionFormat sınıfı"
linktitle: "ReflectionFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ReflectionFormat sınıfı. C++'da bir nesne için yansıma biçimlendirmesini temsil eder."
type: docs
weight: 9500
url: /tr/cpp/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class


Bir nesne için yansıma biçimlendirmesini temsil eder.

```cpp
class ReflectionFormat : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Blur](./get_blur/)() | Yansıma etkisine uygulanan bulanıklık derecesini puan cinsinden belirten double değerini alır veya ayarlar. Varsayılan değer 0.0. |
| [get_Distance](./get_distance/)() | Yansıyan görüntünün nesneden ayrılma miktarını puan cinsinden belirten double değerini alır veya ayarlar. Varsayılan değer 0.0. |
| [get_Size](./get_size/)() | Yansıyan nesnenin yüzde olarak yansıma boyutunu temsil eden 0.0 ile 1.0 arasında bir double değerini alır veya ayarlar. Varsayılan değer 0.0. |
| [get_Transparency](./get_transparency/)() | Yansıma etkisinin şeffaflık derecesini temsil eden 0.0 (opak) ile 1.0 (şeffaf) arasında bir double değerini alır veya ayarlar. Varsayılan değer 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Üst nesneden [ReflectionFormat](./) öğesini kaldırır. |
| [set_Blur](./set_blur/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ReflectionFormat::get_Blur](./get_blur/). |
| [set_Distance](./set_distance/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ReflectionFormat::get_Distance](./get_distance/). |
| [set_Size](./set_size/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ReflectionFormat::get_Size](./get_size/). |
| [set_Transparency](./set_transparency/)(double) | Ayarlayıcı [Aspose::Words::Drawing::ReflectionFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Açıklamalar


Bir nesnenin yansıma özelliklerine erişmek için [Reflection](../shapebase/get_reflection/) özelliğini kullanın. [ReflectionFormat](./) sınıfının örneklerini doğrudan oluşturmazsınız.

## Örnekler



Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Reflection()->set_Transparency(0.37);
shape->get_Reflection()->set_Size(0.48);
shape->get_Reflection()->set_Blur(17.5);
shape->get_Reflection()->set_Distance(9.2);

doc->Save(get_ArtifactsDir() + u"Shape.Reflection.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Reflection.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ReflectionFormat> reflectionFormat = shape->get_Reflection();

ASSERT_NEAR(0.37, reflectionFormat->get_Transparency(), 0.01);
ASSERT_NEAR(0.48, reflectionFormat->get_Size(), 0.01);
ASSERT_NEAR(17.5, reflectionFormat->get_Blur(), 0.01);
ASSERT_NEAR(9.2, reflectionFormat->get_Distance(), 0.01);

reflectionFormat->Remove();

ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Transparency());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Size());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Blur());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Distance());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
