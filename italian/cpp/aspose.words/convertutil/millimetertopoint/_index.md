---
title: "Aspose::Words::ConvertUtil::MillimeterToPoint method"
linktitle: "MillimeterToPoint"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ConvertUtil::MillimeterToPoint method. Converte i millimetri in punti in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil::MillimeterToPoint method


Converte i millimetri in punti.

```cpp
static double Aspose::Words::ConvertUtil::MillimeterToPoint(double millimeters)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| millimetri | double | Il valore da convertire. |

## Esempi



Mostra come specificare le proprietà della pagina in millimetri.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Il "Page Setup" di una sezione definisce la dimensione dei margini della pagina in punti.
// Possiamo anche usare la classe "ConvertUtil" per utilizzare un'unità di misura più familiare,
// come i millimetri quando si definiscono i confini.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(30));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(50));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(80));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(40));

// Un centimetro è approssimativamente 28,3 punti.
ASSERT_NEAR(28.34, Aspose::Words::ConvertUtil::MillimeterToPoint(10), 0.01);

// Aggiungi contenuto per dimostrare i nuovi margini.
builder->Writeln(System::String::Format(u"This Text is {0} points from the left, ", pageSetup->get_LeftMargin()) + System::String::Format(u"{0} points from the right, ", pageSetup->get_RightMargin()) + System::String::Format(u"{0} points from the top, ", pageSetup->get_TopMargin()) + System::String::Format(u"and {0} points from the bottom of the page.", pageSetup->get_BottomMargin()));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndMillimeters.docx");
```

## Vedi anche

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
