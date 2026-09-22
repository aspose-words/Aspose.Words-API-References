---
title: "Aspose::Words::Drawing::ShapeBase::get_IsDecorative yöntemi"
linktitle: "get_IsDecorative"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_IsDecorative yöntemi. C++'de belgedeki şeklin dekoratif olup olmadığını belirten bayrağı alır veya ayarlar."
type: docs
weight: 25000
url: /tr/cpp/aspose.words.drawing/shapebase/get_isdecorative/
---
## ShapeBase::get_IsDecorative method


Şeklin belgede dekoratif olup olmadığını belirten bayrağı alır veya ayarlar.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDecorative()
```


## Örnekler



Şeklin dekoratif olduğunu nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Decorative shapes.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// "AlternativeText" boş değilse, şekil dekoratif olamaz.
// Bu yüzden değerimiz 'false' olarak değişti.
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// Yeni bir şekli dekoratif olarak oluştur.
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(get_ArtifactsDir() + u"Shape.IsDecorative.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
