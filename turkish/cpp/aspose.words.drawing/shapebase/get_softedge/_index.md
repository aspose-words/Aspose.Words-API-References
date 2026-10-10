---
title: "Aspose::Words::Drawing::ShapeBase::get_SoftEdge metodu"
linktitle: "get_SoftEdge"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_SoftEdge metodu. C++'ta şekil için yumuşak kenar biçimlendirmesini alır."
type: docs
weight: 49500
url: /tr/cpp/aspose.words.drawing/shapebase/get_softedge/
---
## ShapeBase::get_SoftEdge method


Şekil için yumuşak kenar biçimlendirmesini alır.

```cpp
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> Aspose::Words::Drawing::ShapeBase::get_SoftEdge()
```


## Örnekler



Yumuşak kenar biçimlendirmesiyle nasıl çalışılacağını gösterir.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Şekle yumuşak kenar uygula.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Yumuşak kenarlı dikdörtgen şekilli belgeyi yükle.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Yumuşak kenar yarıçapını kontrol et.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Şekilden yumuşak kenarı kaldır.
softEdgeFormat->Remove();

// Kaldırılan yumuşak kenarın yarıçapını kontrol edin.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```


Görsel çözünürlüğü sınırlamayı nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Ayrıca Bakınız

* Class [SoftEdgeFormat](../../softedgeformat/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
