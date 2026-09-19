---
title: "Aspose::Words::ConvertUtil::PointToPixel method"
linktitle: "PointToPixel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ConvertUtil::PointToPixel method. Converte i punti in pixel a 96 dpi in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/convertutil/pointtopixel/
---
## ConvertUtil::PointToPixel(double) method


Converte i punti in pixel a 96 dpi.

```cpp
static double Aspose::Words::ConvertUtil::PointToPixel(double points)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| punti | double | Il valore da convertire. |

## Esempi



Mostra come specificare le proprietà della pagina in pixel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Il "Page Setup" di una sezione definisce la dimensione dei margini della pagina in punti.
// Possiamo anche usare la classe "ConvertUtil" per utilizzare un'unità di misura diversa,
// come i pixel quando si definiscono i confini.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::PixelToPoint(200));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::PixelToPoint(225));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::PixelToPoint(125));

// Un pixel è pari a 0,75 punti.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToPixel(0.75));

// Il valore DPI predefinito utilizzato è 96.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1, 96));

// Aggiungi contenuto per dimostrare i nuovi margini.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} pixels from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} pixels from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} pixels from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} pixels from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixels.docx");
```

## Vedi anche

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## ConvertUtil::PointToPixel(double, double) method


Converte i punti in pixel alla risoluzione pixel specificata.

```cpp
static double Aspose::Words::ConvertUtil::PointToPixel(double points, double resolution)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| punti | double | Il valore da convertire. |
| risoluzione | double | La risoluzione dpi (punti per pollice). |

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
