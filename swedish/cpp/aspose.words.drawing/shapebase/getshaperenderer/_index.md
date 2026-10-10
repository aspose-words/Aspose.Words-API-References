---
title: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer‑metod"
linktitle: "GetShapeRenderer"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer‑metod. Skapar och returnerar ett objekt som kan användas för att rendera denna form till en bild i C++."
type: docs
weight: 58000
url: /sv/cpp/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase::GetShapeRenderer method


Skapar och returnerar ett objekt som kan användas för att rendera denna form till en bild.

```cpp
System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> Aspose::Words::Drawing::ShapeBase::GetShapeRenderer()
```


### ReturnValue

Renderingsobjektet för denna form.
## Anmärkningar


Denna metod anropar bara konstruktorn för [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) och skickar detta objekt som en parameter.

## Exempel



Visar hur man använder en formrenderare för att exportera former till filer i det lokala filsystemet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// Det finns 7 former i dokumentet, inklusive en gruppform med 2 underformer.
// Vi kommer att rendera varje form till en bildfil i det lokala filsystemet
// och ignorera gruppformerna eftersom de saknar utseende.
// Detta kommer att producera 6 bildfiler.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## Se även

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
