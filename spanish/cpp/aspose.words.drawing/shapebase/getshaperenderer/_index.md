---
title: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer método"
linktitle: "GetShapeRenderer"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer método. Crea y devuelve un objeto que puede usarse para renderizar esta forma en una imagen en C++."
type: docs
weight: 58000
url: /es/cpp/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase::GetShapeRenderer method


Crea y devuelve un objeto que puede usarse para renderizar esta forma en una imagen.

```cpp
System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> Aspose::Words::Drawing::ShapeBase::GetShapeRenderer()
```


### ReturnValue

El objeto renderizador para esta forma.
## Observaciones


Este método simplemente invoca el constructor de [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) y pasa este objeto como parámetro.

## Ejemplos



Muestra cómo usar un renderizador de formas para exportar formas a archivos en el sistema de archivos local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// Hay 7 formas en el documento, incluyendo una forma de grupo con 2 formas secundarias.
// Renderizaremos cada forma a un archivo de imagen en el sistema de archivos local
// mientras se ignoran los grupos de formas ya que no tienen apariencia.
// Esto producirá 6 archivos de imagen.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## Ver también

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
