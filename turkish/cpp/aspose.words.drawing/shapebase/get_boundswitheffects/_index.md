---
title: "Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects metodu"
linktitle: "get_BoundsWithEffects"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects metodu. Çizim efektleri uygulandıktan sonra bu şekil nesnesinin sahip olduğu son boyutu alır. Değer C++'ta puan cinsinden ölçülür."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.drawing/shapebase/get_boundswitheffects/
---
## ShapeBase::get_BoundsWithEffects method


Çizim efektleri uygulandıktan sonra bu şekil nesnesinin sahip olduğu son kapsamı alır. Değer nokta cinsinden ölçülür.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsWithEffects()
```


## Örnekler



Bir şeklin sınırlarının şekil efektleri tarafından nasıl etkilendiğini kontrol etmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape shadow effect.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// İki şekil, boyutlar ve şekil tipi açısından özdeştir.
ASPOSE_ASSERT_EQ(shapes[0]->get_Width(), shapes[1]->get_Width());
ASPOSE_ASSERT_EQ(shapes[0]->get_Height(), shapes[1]->get_Height());
ASSERT_EQ(shapes[0]->get_ShapeType(), shapes[1]->get_ShapeType());

// İlk şeklin hiçbir etkisi yoktur, ikinci şeklin ise bir gölgesi ve kalın bir kenarlığı vardır.
// Bu efektler, ikinci şeklin siluetinin boyutunu birinciden daha büyük yapar.
// Microsoft Word'de bu şekillere tıkladığımızda dikdörtgenin boyutu görünsede,
// İkinci şeklin görünen dış sınırları gölge ve kenarlık tarafından etkilenir ve bu yüzden daha büyüktür.
// "AdjustWithEffects" metodunu kullanarak şeklin gerçek boyutunu görebiliriz.
ASPOSE_ASSERT_EQ(0.0, shapes[0]->get_StrokeWeight());
ASPOSE_ASSERT_EQ(20.0, shapes[1]->get_StrokeWeight());
ASSERT_FALSE(shapes[0]->get_ShadowEnabled());
ASSERT_TRUE(shapes[1]->get_ShadowEnabled());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = shapes[0];

// Bir dikdörtgeni temsil eden RectangleF nesnesi oluşturun,
// bu nesneyi potansiyel olarak bir şeklin koordinatları ve sınırları için kullanabiliriz.
System::Drawing::RectangleF rectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);

// Bu metodu çalıştırarak dikdörtgenin tüm şekil efektlerine göre ayarlanmış boyutunu elde edin.
System::Drawing::RectangleF rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Şeklin kenar değiştiren bir etkisi olmadığından, sınır boyutları etkilenmez.
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(200, rectangleFOut.get_Y());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1000, rectangleFOut.get_Height());

// İlk şeklin son kapsamını puan cinsinden doğrulayın.
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(0, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(147, shape->get_BoundsWithEffects().get_Height());

shape = shapes[1];
rectangleF = System::Drawing::RectangleF(200.0f, 200.0f, 1000.0f, 1000.0f);
rectangleFOut = shape->AdjustWithEffects(rectangleF);

// Şekil efektleri, şeklin görünen sol üst köşesini hafifçe kaydırdı.
ASPOSE_ASSERT_EQ(171.5, rectangleFOut.get_X());
ASPOSE_ASSERT_EQ(167, rectangleFOut.get_Y());

// Efektler ayrıca şeklin görünen boyutlarını etkiledi.
ASPOSE_ASSERT_EQ(1045, rectangleFOut.get_Width());
ASPOSE_ASSERT_EQ(1133.5, rectangleFOut.get_Height());

// Efektler ayrıca şeklin görünen sınırlarını etkiledi.
ASPOSE_ASSERT_EQ(-28.5, shape->get_BoundsWithEffects().get_X());
ASPOSE_ASSERT_EQ(-33, shape->get_BoundsWithEffects().get_Y());
ASPOSE_ASSERT_EQ(192, shape->get_BoundsWithEffects().get_Width());
ASPOSE_ASSERT_EQ(280.5, shape->get_BoundsWithEffects().get_Height());
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
