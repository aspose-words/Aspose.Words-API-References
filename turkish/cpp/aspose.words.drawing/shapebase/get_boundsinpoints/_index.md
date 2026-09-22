---
title: "Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints yöntemi"
linktitle: "get_BoundsInPoints"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints yöntemi. Şeklin içerik bloğunun konumunu ve boyutunu, puan cinsinden, en üstteki şeklin çapa göre C++'da alır."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.drawing/shapebase/get_boundsinpoints/
---
## ShapeBase::get_BoundsInPoints method


En üst şeklin çapa noktasına göre, şeklin içinde bulunduğu bloğun konumunu ve boyutunu nokta cinsinden alır.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints()
```


## Örnekler



Şeklin içerik bloğu sınırlarını nasıl doğrulayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Line, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 50, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_StrokeColor(System::Drawing::Color::get_Orange());

// Satır kendisi belge sayfasında çok az yer kaplasa da,
// dikdörtgen bir içerik bloğu kaplar ve bu bloğun boyutunu "Bounds" özelliklerini kullanarak belirleyebiliriz.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

// Bir grup şekil oluşturun ve ardından "Bounds" özelliğini kullanarak içerik bloğunun boyutunu ayarlayın.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// Bir dikdörtgen oluşturun, sınırlayıcı bloğunun boyutunu doğrulayın ve ardından grup şekline ekleyin.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), shape->get_BoundsInPoints());

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Grup şeklinin koordinat düzlemi, içerik bloğunun sol üst köşesinde bir orijine sahiptir,
// ve (1000, 1000) koordinatları sağ alt köşededir.
// Grup şeklimiz 250x250pt boyutundadır, bu yüzden grup şeklinin koordinat düzlemindeki her 4pt
// belge gövdesinin koordinat düzleminde 1pt'ye karşılık gelir.
// Eklediğimiz her şekil de boyut olarak 4 kat küçülecektir.
// Şeklin "BoundsInPoints" özelliğindeki değişiklik bunu yansıtacaktır.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

// Bir şekil ekleyin ve onu grup şeklinin içerik bloğu sınırlarının dışına yerleştirin.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Grup şeklinin belge gövdesindeki ayak izi arttı, ancak içerik bloğu aynı kaldı.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(get_ArtifactsDir() + u"Shape.Bounds.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
