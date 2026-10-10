---
title: "Aspose::Words::Drawing::SoftEdgeFormat class"
linktitle: "SoftEdgeFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::SoftEdgeFormat class. Representa el formato de borde suave para un objeto en C++."
type: docs
weight: 13500
url: /es/cpp/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class


Representa el formato de borde suave para un objeto.

```cpp
class SoftEdgeFormat : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Radius](./get_radius/)() | Obtiene o establece un valor double que representa la longitud del radio para un efecto de borde suave en puntos (pt). El valor predeterminado es 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Elimina [SoftEdgeFormat](./) del objeto padre. |
| [set_Radius](./set_radius/)(double) | Setter para [Aspose::Words::Drawing::SoftEdgeFormat::get_Radius](./get_radius/). |
| static [Type](./type/)() |  |
## Observaciones


Utilice la propiedad [SoftEdge](../shapebase/get_softedge/) para acceder a las propiedades de borde suave de un objeto. No crea instancias de la clase [SoftEdgeFormat](./) directamente.

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

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
