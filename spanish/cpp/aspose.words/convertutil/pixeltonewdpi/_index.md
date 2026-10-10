---
title: "Aspose::Words::ConvertUtil::PixelToNewDpi método"
linktitle: "PixelToNewDpi"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ConvertUtil::PixelToNewDpi método. Convierte píxeles de una resolución a otra en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil::PixelToNewDpi method


Convierte píxeles de una resolución a otra.

```cpp
static int32_t Aspose::Words::ConvertUtil::PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| píxeles | double | El valor a convertir. |
| oldDpi | double | La resolución dpi actual (puntos por pulgada). |
| newDpi | double | La nueva resolución dpi (puntos por pulgada). |

## Ejemplos



Muestra cómo convertir puntos a píxeles con resolución predeterminada y personalizada.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Define el tamaño del margen superior de esta sección en píxeles, según un DPI personalizado.
const double myDpi = 192;

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// Con el DPI predeterminado de 96, un píxel equivale a 0,75 puntos.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));

builder->Writeln(System::String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + System::String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// Establece un nuevo DPI y ajusta el valor del margen superior en consecuencia.
const double newDpi = 300;
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(System::String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + u"pixels from the top of the page.");

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## Ver también

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
