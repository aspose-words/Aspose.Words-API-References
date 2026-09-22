---
title: "Aspose::Words::Drawing::GradientStopCollection sınıfı"
linktitle: "GradientStopCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::GradientStopCollection sınıfı. GradientStop nesnelerinden oluşan bir koleksiyon içerir. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class


GradientStop nesnelerinden oluşan bir koleksiyon içerir. Daha fazla bilgi edinmek için [Graphic Elements ile Çalışma](https://docs.aspose.com/words/cpp/working-with-graphic-elements/) belge makalesini ziyaret edin.

```cpp
class GradientStopCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::GradientStop>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Belirtilen bir [GradientStop](../gradientstop/) öğesini bir degradeye ekler. |
| [get_Count](./get_count/)() | Koleksiyondaki öğe sayısını gösteren bir tam sayı değeri alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyon içinde yineleme yapan bir döngücü (enumerator) döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Koleksiyondaki bir [GradientStop](../gradientstop/) nesnesini alır veya ayarlar. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Koleksiyondaki bir [GradientStop](../gradientstop/) nesnesini alır veya ayarlar. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Belirtilen bir indekste koleksiyona bir [GradientStop](../gradientstop/) ekler. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Drawing::GradientStop\>\&) | Koleksiyondan belirtilen bir [GradientStop](../gradientstop/) öğesini kaldırır. |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen bir indekste koleksiyondan bir [GradientStop](../gradientstop/) öğesini kaldırır. |
| static [Type](./type/)() |  |

## Örnekler



Degrade doldurmasına gradient durakları eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
shape->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Green(), System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2);

// Gradient durakları koleksiyonunu al.
System::SharedPtr<Aspose::Words::Drawing::GradientStopCollection> gradientStops = shape->get_Fill()->get_GradientStops();

// İlk gradient durakını değiştir.
gradientStops->idx_get(0)->set_Color(System::Drawing::Color::get_Aqua());
gradientStops->idx_get(0)->set_Position(0.1);
gradientStops->idx_get(0)->set_Transparency(0.25);

// Koleksiyonun sonuna yeni bir gradient durak ekle.
auto gradientStop = System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Brown(), 0.5);
gradientStops->Add(gradientStop);

// 1. indeksteki gradient durakını kaldır.
gradientStops->RemoveAt(1);
// Ve aynı 1. indekse yeni bir gradient durak ekle.
gradientStops->Insert(1, System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Chocolate(), 0.75, 0.3));

// Koleksiyondaki son gradient durakını kaldır.
gradientStop = gradientStops->idx_get(2);
gradientStops->Remove(gradientStop);

ASSERT_EQ(2, gradientStops->get_Count());

ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 0, 255, 255), gradientStops->idx_get(0)->get_BaseColor());
ASSERT_EQ(System::Drawing::Color::get_Aqua().ToArgb(), gradientStops->idx_get(0)->get_Color().ToArgb());
ASSERT_NEAR(0.1, gradientStops->idx_get(0)->get_Position(), 0.01);
ASSERT_NEAR(0.25, gradientStops->idx_get(0)->get_Transparency(), 0.01);

ASSERT_EQ(System::Drawing::Color::get_Chocolate().ToArgb(), gradientStops->idx_get(1)->get_Color().ToArgb());
ASSERT_NEAR(0.75, gradientStops->idx_get(1)->get_Position(), 0.01);
ASSERT_NEAR(0.3, gradientStops->idx_get(1)->get_Transparency(), 0.01);

// Şekli DML kullanarak tanımlamak için uyumluluk seçeneğini kullan.
// belge kaydedildikten sonra "GradientStops" özelliğini almak istiyorsanız.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientStops.docx", saveOptions);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
