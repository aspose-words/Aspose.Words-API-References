---
title: "Aspose::Words::Drawing::GradientStop::Remove yöntemi"
linktitle: "Remove"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::GradientStop::Remove yöntemi. C++'ta gradient durak noktasını üst GradientStopCollection'dan kaldırır."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.drawing/gradientstop/remove/
---
## GradientStop::Remove method


Gradient durak noktasını üst [GradientStopCollection](../../gradientstopcollection/) koleksiyonundan kaldırır.

```cpp
void Aspose::Words::Drawing::GradientStop::Remove()
```


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

* Class [GradientStop](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
