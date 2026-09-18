---
title: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer Methode"
linktitle: "GetShapeRenderer"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer Methode. Erstellt und gibt ein Objekt zurück, das verwendet werden kann, um diese Form in C++ in ein Bild zu rendern."
type: docs
weight: 58000
url: /de/cpp/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase::GetShapeRenderer method


Erstellt und gibt ein Objekt zurück, das verwendet werden kann, um diese Form in ein Bild zu rendern.

```cpp
System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> Aspose::Words::Drawing::ShapeBase::GetShapeRenderer()
```


### ReturnValue

Das Renderer-Objekt für diese Form.
## Hinweise


Diese Methode ruft lediglich den Konstruktor von [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) auf und übergibt dieses Objekt als Parameter.

## Beispiele



Zeigt, wie ein ShapeRenderer verwendet wird, um Formen in Dateien im lokalen Dateisystem zu exportieren.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// Im Dokument befinden sich 7 Formen, einschließlich einer Gruppenform mit 2 untergeordneten Formen.
// Wir werden jede Form in eine Bilddatei im lokalen Dateisystem rendern
// während wir die Gruppenformen ignorieren, da sie keine Darstellung haben.
// Dies wird 6 Bilddateien erzeugen.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## Siehe auch

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
