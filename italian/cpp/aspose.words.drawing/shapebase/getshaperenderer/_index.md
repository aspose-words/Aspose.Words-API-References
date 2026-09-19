---
title: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer metodo"
linktitle: "GetShapeRenderer"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer metodo. Crea e restituisce un oggetto che può essere usato per renderizzare questa forma in un'immagine in C++."
type: docs
weight: 58000
url: /it/cpp/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase::GetShapeRenderer method


Crea e restituisce un oggetto che può essere usato per renderizzare questa forma in un'immagine.

```cpp
System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> Aspose::Words::Drawing::ShapeBase::GetShapeRenderer()
```


### ReturnValue

L'oggetto renderer per questa forma.
## Note


Questo metodo invoca semplicemente il costruttore di [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) e passa questo oggetto come parametro.

## Esempi



Mostra come utilizzare un renderer di forme per esportare le forme in file nel file system locale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// Ci sono 7 forme nel documento, inclusa una forma di gruppo con 2 forme figlie.
// Renderizzeremo ogni forma in un file immagine nel file system locale
// ignorando le forme di gruppo poiché non hanno alcun aspetto.
// Questo produrrà 6 file immagine.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## Vedi anche

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
