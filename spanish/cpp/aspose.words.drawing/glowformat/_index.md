---
title: "Clase Aspose::Words::Drawing::GlowFormat"
linktitle: "GlowFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::GlowFormat. Representa el formato de resplandor para un objeto en C++."
type: docs
weight: 1500
url: /es/cpp/aspose.words.drawing/glowformat/
---
## GlowFormat class


Representa el formato de brillo para un objeto.

```cpp
class GlowFormat : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Color](./get_color/)() | Obtiene o establece un objeto **Color** que representa el color para un efecto de resplandor. El valor predeterminado es **Black**. |
| [get_Radius](./get_radius/)() | Obtiene o establece un valor double que representa la longitud del radio para un efecto de resplandor en puntos (pt). El valor predeterminado es 0.0. |
| [get_Transparency](./get_transparency/)() | Obtiene o establece el grado de transparencia para el efecto de resplandor como un valor entre 0.0 (opaco) y 1.0 (claro). El valor predeterminado es 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Elimina [GlowFormat](./) del objeto padre. |
| [set_Color](./set_color/)(System::Drawing::Color) | Método set para [Aspose::Words::Drawing::GlowFormat::get_Color](./get_color/). |
| [set_Radius](./set_radius/)(double) | Método set para [Aspose::Words::Drawing::GlowFormat::get_Radius](./get_radius/). |
| [set_Transparency](./set_transparency/)(double) | Método set para [Aspose::Words::Drawing::GlowFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Observaciones


Utilice la propiedad [Glow](../shapebase/get_glow/) para acceder a las propiedades de resplandor de un objeto. No crea instancias de la clase [GlowFormat](./) directamente.

## Ejemplos



Muestra cómo interactuar con el efecto de forma de resplandor.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Glow()->set_Color(System::Drawing::Color::get_Salmon());
shape->get_Glow()->set_Radius(30);
shape->get_Glow()->set_Transparency(0.15);

doc->Save(get_ArtifactsDir() + u"Shape.Glow.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Glow.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::Drawing::Color::FromArgb(217, 250, 128, 114).ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(30, shape->get_Glow()->get_Radius());
ASSERT_NEAR(0.15, shape->get_Glow()->get_Transparency(), 0.01);

shape->get_Glow()->Remove();

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Radius());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Transparency());
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
