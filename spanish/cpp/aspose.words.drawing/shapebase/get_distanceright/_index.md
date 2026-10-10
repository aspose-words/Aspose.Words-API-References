---
title: "Aspose::Words::Drawing::ShapeBase::get_DistanceRight método"
linktitle: "get_DistanceRight"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_DistanceRight método. Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde derecho de la forma en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words.drawing/shapebase/get_distanceright/
---
## ShapeBase::get_DistanceRight method


Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde derecho de la forma.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_DistanceRight()
```

## Observaciones


El valor predeterminado es 1/8 de pulgada.

Tiene efecto solo para formas de nivel superior.

## Ejemplos



Muestra cómo establecer la distancia de ajuste para un texto que rodea una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte un rectángulo y haga que el texto se ajuste estrechamente a sus límites.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 150, 150);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Tight);

// Establezca la distancia mínima entre la forma y el texto circundante a 40pt en todos los lados.
shape->set_DistanceTop(40);
shape->set_DistanceBottom(40);
shape->set_DistanceLeft(40);
shape->set_DistanceRight(40);

// Mueva la forma más cerca del centro de la página y luego gire la forma 60 grados en sentido horario.
shape->set_Top(75);
shape->set_Left(150);
shape->set_Rotation(60);

// Agregue texto que se ajuste alrededor de la forma.
builder->get_Font()->set_Size(24);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"Shape.Coordinates.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
