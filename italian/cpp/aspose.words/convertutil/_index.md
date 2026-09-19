---
title: "Aspose::Words::ConvertUtil class"
linktitle: "ConvertUtil"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ConvertUtil class. Fornisce funzioni di supporto per convertire tra varie unità di misura. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words/convertutil/
---
## ConvertUtil class


Fornisce funzioni di supporto per convertire tra varie unità di misura. Per saperne di più, visita l'articolo di documentazione [Convert Between Measurement Units](https://docs.aspose.com/words/cpp/convert-between-measurement-units/).

```cpp
class ConvertUtil
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ConvertUtil](./convertutil/)() |  |
| static [InchToPoint](./inchtopoint/)(double) | Converte i pollici in punti. |
| static [MillimeterToPoint](./millimetertopoint/)(double) | Converte i millimetri in punti. |
| static [PixelToNewDpi](./pixeltonewdpi/)(double, double, double) | Converte i pixel da una risoluzione all'altra. |
| static [PixelToPoint](./pixeltopoint/)(double) | Converte i pixel in punti a 96 dpi. |
| static [PixelToPoint](./pixeltopoint/)(double, double) | Converte i pixel in punti alla risoluzione pixel specificata. |
| static [PointToInch](./pointtoinch/)(double) | Converte i punti in pollici. |
| static [PointToPixel](./pointtopixel/)(double) | Converte i punti in pixel a 96 dpi. |
| static [PointToPixel](./pointtopixel/)(double, double) | Converte i punti in pixel alla risoluzione pixel specificata. |

## Esempi



Mostra come regolare le dimensioni della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```


Mostra come specificare le proprietà della pagina in pollici.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Il "Page Setup" di una sezione definisce la dimensione dei margini della pagina in punti.
// Possiamo anche usare la classe "ConvertUtil" per utilizzare un'unità di misura più familiare,
// come i pollici quando si definiscono i confini.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));

// Un pollice è pari a 72 punti.
ASPOSE_ASSERT_EQ(72.0, Aspose::Words::ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToInch(72));

// Aggiungi contenuto per dimostrare i nuovi margini.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndInches.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
