---
title: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer metodu"
linktitle: "GetShapeRenderer"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer metodu. C++'ta bu şekli bir görüntüye renderlemek için kullanılabilecek bir nesne oluşturur ve döndürür."
type: docs
weight: 58000
url: /tr/cpp/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase::GetShapeRenderer method


Bu şekli bir görüntüye renderlemek için kullanılabilecek bir nesne oluşturur ve döndürür.

```cpp
System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> Aspose::Words::Drawing::ShapeBase::GetShapeRenderer()
```


### ReturnValue

Bu şekil için renderleyici nesnesi.
## Açıklamalar


Bu metod sadece [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) yapıcısını çağırır ve bu nesneyi parametre olarak geçirir.

## Örnekler



Yerel dosya sisteminde şekilleri dosyalara dışa aktarmak için bir şekil renderleyicisinin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// Belgede 7 şekil var, bunlar arasında 2 alt şekle sahip bir grup şekil de bulunuyor.
// Her şekli yerel dosya sisteminde bir görüntü dosyasına renderleyeceğiz.
// grup şekillerini görünümleri olmadığı için yok sayarken.
// Bu, 6 görüntü dosyası üretecek.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## Ayrıca Bakınız

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
