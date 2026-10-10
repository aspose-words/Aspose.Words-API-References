---
title: "Aspose::Words::ConvertUtil::PixelToNewDpi metodo"
linktitle: "PixelToNewDpi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ConvertUtil::PixelToNewDpi metodo. Converte i pixel da una risoluzione all'altra in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil::PixelToNewDpi method


Converte i pixel da una risoluzione all'altra.

```cpp
static int32_t Aspose::Words::ConvertUtil::PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pixel | double | Il valore da convertire. |
| oldDpi | double | La risoluzione dpi (punti per pollice) corrente. |
| newDpi | double | La nuova risoluzione dpi (punti per pollice). |

## Esempi



Mostra come utilizzare la conversione da punti a pixel con risoluzione predefinita e personalizzata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Definisci la dimensione del margine superiore di questa sezione in pixel, secondo un DPI personalizzato.
const double myDpi = 192;

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// Con il DPI predefinito di 96, un pixel è 0,75 punti.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));

builder->Writeln(System::String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + System::String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// Imposta un nuovo DPI e regola di conseguenza il valore del margine superiore.
const double newDpi = 300;
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(System::String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + u"pixels from the top of the page.");

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## Vedi anche

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
