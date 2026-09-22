---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInline yöntemi"
linktitle: "get_IsInline"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInline yöntemi. C++'da bu şeklin metinle satır içi konumlandırılıp konumlandırılmadığını hızlı bir şekilde belirlemenin yolu."
type: docs
weight: 30000
url: /tr/cpp/aspose.words.drawing/shapebase/get_isinline/
---
## ShapeBase::get_IsInline method


Bu şeklin metin içinde satır içi konumlandırılıp konumlandırılmadığını belirlemenin hızlı bir yolu.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInline()
```

## Açıklamalar


Yalnızca üst düzey şekiller için etkilidir.

## Örnekler



Bir şeklin satır içi mi yoksa yüzen mi olduğunu nasıl belirleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 -  Satır içi:
builder->Write(u"Hello world! ");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());
builder->Write(u" Hello again.");

// Satır içi bir şekil, metin akışları gibi diğer paragraf öğeleri arasında bir paragraf içinde bulunur.
// Microsoft Word'de, şekli bir karakter gibi herhangi bir paragrafa tıklayıp sürükleyebiliriz.
// Şekil büyükse, dikey paragraf aralığını etkiler.
// Bu şekli paragrafı olmayan bir konuma taşıyamayız.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::Inline, shape->get_WrapType());
ASSERT_TRUE(shape->get_IsInline());

// 2 -  Yüzen:
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

// Yüzen bir şekil, eklediğimiz paragrafın içinde yer alır,
// Şekle tıkladığımızda görünen bir çapa simgesiyle bunu belirleyebiliriz.
// Şeklin sol tarafında görünür bir çapa simgesi yoksa,
// Görünür çapa "Options" -> "Display" -> "Object Anchors" yoluyla etkinleştirmemiz gerekir.
// Microsoft Word'de, bu şekle sol tıklayıp sürükleyerek istediğimiz konuma serbestçe taşıyabiliriz.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, shape->get_WrapType());
ASSERT_FALSE(shape->get_IsInline());

doc->Save(get_ArtifactsDir() + u"Shape.IsInline.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
