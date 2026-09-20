---
title: "Aspose::Words::Drawing::SoftEdgeFormat::Remove método"
linktitle: "Remove"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::SoftEdgeFormat::Remove método. Elimina SoftEdgeFormat del objeto padre en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.drawing/softedgeformat/remove/
---
## SoftEdgeFormat::Remove method


Elimina [SoftEdgeFormat](../) del objeto padre.

```cpp
void Aspose::Words::Drawing::SoftEdgeFormat::Remove()
```


## Ejemplos



Muestra cómo trabajar con el formato de borde suave.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Aplique borde suave a la forma.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Cargue un documento con una forma rectangular con borde suave.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Verifique el radio del borde suave.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Eliminar el borde suave de la forma.
softEdgeFormat->Remove();

// Verificar el radio del borde suave eliminado.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```


Muestra cómo establecer un límite para la resolución de imágenes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## Ver también

* Class [SoftEdgeFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
