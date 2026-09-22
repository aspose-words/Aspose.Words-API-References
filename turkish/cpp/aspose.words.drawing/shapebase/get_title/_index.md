---
title: "Aspose::Words::Drawing::ShapeBase::get_Title metodu"
linktitle: "get_Title"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_Title metodu. C++'ta geçerli şekil nesnesinin başlığını (alt yazısını) alır veya ayarlar."
type: docs
weight: 51000
url: /tr/cpp/aspose.words.drawing/shapebase/get_title/
---
## ShapeBase::get_Title method


Mevcut şekil nesnesinin başlığını (alt yazısını) alır veya ayarlar.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Title()
```

## Açıklamalar


Varsayılan boş dizedir.

**null** olamaz, ancak boş bir dize olabilir.

## Örnekler



Bir şeklin başlığının nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir şekil oluşturun, ona bir başlık verin ve ardından belgeye ekleyin.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// Başlığı olan bir şekil içeren bir belgeyi kaydettiğimizde,
// Aspose.Words bu başlığı şeklin Alt Metni'nde depolar.
doc->Save(get_ArtifactsDir() + u"Shape.Title.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Title.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
