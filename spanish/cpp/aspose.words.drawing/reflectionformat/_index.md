---
title: "Aspose::Words::Drawing::ReflectionFormat clase"
linktitle: "ReflectionFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ReflectionFormat clase. Representa el formato de reflexión para un objeto en C++."
type: docs
weight: 9500
url: /es/cpp/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class


Representa el formato de reflexión para un objeto.

```cpp
class ReflectionFormat : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Blur](./get_blur/)() | Obtiene o establece un valor double que especifica el grado del efecto de desenfoque aplicado al efecto de reflexión en puntos. El valor predeterminado es 0.0. |
| [get_Distance](./get_distance/)() | Obtiene o establece un valor double que especifica la cantidad de separación de la imagen reflejada del objeto en puntos. El valor predeterminado es 0.0. |
| [get_Size](./get_size/)() | Obtiene o establece un valor double entre 0.0 y 1.0 que representa el tamaño de la reflexión como un porcentaje del objeto reflejado. El valor predeterminado es 0.0. |
| [get_Transparency](./get_transparency/)() | Obtiene o establece un valor double entre 0.0 (opaco) y 1.0 (claro) que representa el grado de transparencia del efecto de reflexión. El valor predeterminado es 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Elimina [ReflectionFormat](./) del objeto padre. |
| [set_Blur](./set_blur/)(double) | Método set para [Aspose::Words::Drawing::ReflectionFormat::get_Blur](./get_blur/). |
| [set_Distance](./set_distance/)(double) | Método set para [Aspose::Words::Drawing::ReflectionFormat::get_Distance](./get_distance/). |
| [set_Size](./set_size/)(double) | Método set para [Aspose::Words::Drawing::ReflectionFormat::get_Size](./get_size/). |
| [set_Transparency](./set_transparency/)(double) | Método set para [Aspose::Words::Drawing::ReflectionFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Observaciones


Utilice la propiedad [Reflection](../shapebase/get_reflection/) para acceder a las propiedades de reflexión de un objeto. No crea instancias de la clase [ReflectionFormat](./) directamente.

## Ejemplos



Muestra cómo interactuar con el efecto de forma de reflexión.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Reflection()->set_Transparency(0.37);
shape->get_Reflection()->set_Size(0.48);
shape->get_Reflection()->set_Blur(17.5);
shape->get_Reflection()->set_Distance(9.2);

doc->Save(get_ArtifactsDir() + u"Shape.Reflection.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Reflection.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ReflectionFormat> reflectionFormat = shape->get_Reflection();

ASSERT_NEAR(0.37, reflectionFormat->get_Transparency(), 0.01);
ASSERT_NEAR(0.48, reflectionFormat->get_Size(), 0.01);
ASSERT_NEAR(17.5, reflectionFormat->get_Blur(), 0.01);
ASSERT_NEAR(9.2, reflectionFormat->get_Distance(), 0.01);

reflectionFormat->Remove();

ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Transparency());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Size());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Blur());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Distance());
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
