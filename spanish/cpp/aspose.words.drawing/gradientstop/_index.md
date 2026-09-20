---
title: "Clase Aspose::Words::Drawing::GradientStop"
linktitle: "GradientStop"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::GradientStop. Representa una parada de degradado. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.drawing/gradientstop/
---
## GradientStop class


Representa una parada de degradado. Para obtener más información, visite el artículo de documentación [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class GradientStop : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BaseColor](./get_basecolor/)() | Obtiene un valor que representa el color de la parada de degradado sin ningún modificador. |
| [get_Color](./get_color/)() | Obtiene o establece un valor que representa el color de la parada de degradado. |
| [get_Position](./get_position/)() const | Obtiene o establece un valor que representa la posición de una parada dentro del degradado expresada como un porcentaje en el rango de 0.0 a 1.0. |
| [get_Transparency](./get_transparency/)() const | Obtiene o establece un valor que representa la transparencia del relleno de degradado expresada como un porcentaje en el rango de 0.0 a 1.0. |
| [GetType](./gettype/)() const override |  |
| [GradientStop](./gradientstop/)(System::Drawing::Color, double) | Inicializa una nueva instancia de la clase [GradientStop](./). |
| [GradientStop](./gradientstop/)(System::Drawing::Color, double, double) | Inicializa una nueva instancia de la clase [GradientStop](./). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Elimina la parada de degradado del [GradientStopCollection](../gradientstopcollection/) padre. |
| [set_Color](./set_color/)(System::Drawing::Color) | Método set para [Aspose::Words::Drawing::GradientStop::get_Color](./get_color/). |
| [set_Position](./set_position/)(double) | Método set para [Aspose::Words::Drawing::GradientStop::get_Position](./get_position/). |
| [set_Transparency](./set_transparency/)(double) | Método set para [Aspose::Words::Drawing::GradientStop::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo agregar paradas de degradado al relleno del degradado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
shape->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Green(), System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2);

// Obtener la colección de paradas de degradado.
System::SharedPtr<Aspose::Words::Drawing::GradientStopCollection> gradientStops = shape->get_Fill()->get_GradientStops();

// Cambiar la primera parada de degradado.
gradientStops->idx_get(0)->set_Color(System::Drawing::Color::get_Aqua());
gradientStops->idx_get(0)->set_Position(0.1);
gradientStops->idx_get(0)->set_Transparency(0.25);

// Agregar una nueva parada de degradado al final de la colección.
auto gradientStop = System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Brown(), 0.5);
gradientStops->Add(gradientStop);

// Eliminar la parada de degradado en el índice 1.
gradientStops->RemoveAt(1);
// Y insertar una nueva parada de degradado en el mismo índice 1.
gradientStops->Insert(1, System::MakeObject<Aspose::Words::Drawing::GradientStop>(System::Drawing::Color::get_Chocolate(), 0.75, 0.3));

// Eliminar la última parada de degradado en la colección.
gradientStop = gradientStops->idx_get(2);
gradientStops->Remove(gradientStop);

ASSERT_EQ(2, gradientStops->get_Count());

ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 0, 255, 255), gradientStops->idx_get(0)->get_BaseColor());
ASSERT_EQ(System::Drawing::Color::get_Aqua().ToArgb(), gradientStops->idx_get(0)->get_Color().ToArgb());
ASSERT_NEAR(0.1, gradientStops->idx_get(0)->get_Position(), 0.01);
ASSERT_NEAR(0.25, gradientStops->idx_get(0)->get_Transparency(), 0.01);

ASSERT_EQ(System::Drawing::Color::get_Chocolate().ToArgb(), gradientStops->idx_get(1)->get_Color().ToArgb());
ASSERT_NEAR(0.75, gradientStops->idx_get(1)->get_Position(), 0.01);
ASSERT_NEAR(0.3, gradientStops->idx_get(1)->get_Transparency(), 0.01);

// Utilice la opción de cumplimiento para definir la forma usando DML
// si desea obtener la propiedad "GradientStops" después de que el documento se guarde.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientStops.docx", saveOptions);
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
