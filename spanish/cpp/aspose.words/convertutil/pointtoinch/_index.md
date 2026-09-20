---
title: "Aspose::Words::ConvertUtil::PointToInch método"
linktitle: "PointToInch"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ConvertUtil::PointToInch método. Convierte puntos a pulgadas en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil::PointToInch method


Convierte puntos a pulgadas.

```cpp
static double Aspose::Words::ConvertUtil::PointToInch(double points)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| puntos | double | El valor a convertir. |

## Ejemplos



Muestra cómo especificar las propiedades de página en pulgadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// El "Page Setup" de una sección define el tamaño de los márgenes de la página en puntos.
// También podemos usar la clase "ConvertUtil" para utilizar una unidad de medida más familiar,
// como pulgadas al definir los límites.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));

// Una pulgada equivale a 72 puntos.
ASPOSE_ASSERT_EQ(72.0, Aspose::Words::ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToInch(72));

// Agregue contenido para demostrar los nuevos márgenes.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndInches.docx");
```

## Ver también

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
