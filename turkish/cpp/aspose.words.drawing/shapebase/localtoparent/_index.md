---
title: "Aspose::Words::Drawing::ShapeBase::LocalToParent yöntemi"
linktitle: "LocalToParent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::LocalToParent yöntemi. C++'ta bir değeri yerel koordinat alanından üst şeklin koordinat alanına dönüştürür."
type: docs
weight: 61000
url: /tr/cpp/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase::LocalToParent method


Bir değeri yerel koordinat alanından üst şeklin koordinat alanına dönüştürür.

```cpp
System::Drawing::PointF Aspose::Words::Drawing::ShapeBase::LocalToParent(System::Drawing::PointF value)
```


## Örnekler



Bir şeklin koordinat düzlemindeki x ve y konumunun ebeveyn şeklinin koordinat düzlemine nasıl çevrileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir grup şekli ekleyin ve onu aşağıdan 100 puan ve sağdan 100 puan uzaklıkta konumlandırın
// belgenin x ve Y koordinat başlangıç noktasının.
auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// "LocalToParent" metodunu kullanarak grubun iç x ve y koordinatlarında (0, 0) noktasının
// (100, 100) ebeveyn şeklinin koordinat sisteminde bulunduğunu belirleyin. Grup şeklinin ebeveyni doğrudan belgedir.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// Varsayılan olarak, bir şeklin iç koordinat düzleminin sol üst köşesi (0, 0) konumundadır,
// ve sağ alt köşesi (1000, 1000) konumundadır. Boyutu nedeniyle, grup şeklimiz 500pt x 500pt bir alanı kaplar
// belgenin düzleminde. Bu, belgenin koordinat düzleminde 1pt'lik bir hareketin
// grup şeklinin koordinat düzleminde 2pt'lik bir harekete dönüşeceği anlamına gelir.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Grup şeklinin x ve y ekseninin orijini üst sol köşeden merkeze taşıyın.
// Bu, grup içindeki koordinatları belge koordinatlarına göre daha da kaydıracaktır.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Koordinat düzleminin ölçeğini değiştirmek, göreceli konumları da etkileyecektir.
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Bu gruba bir şekil eklemek ve konumunu belgede bir konuma göre tanımlamak istiyorsak,
// öncelikle grup şekli içinde belgenin konumuyla eşleşecek bir konumu doğrulamamız gerekir.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(700.0f, 700.0f), group->LocalToParent(System::Drawing::PointF(350.0f, 350.0f)));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::GroupShape>>(group);

doc->Save(get_ArtifactsDir() + u"Shape.LocalToParent.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
