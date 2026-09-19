---
title: "Aspose::Words::Border::get_TintAndShade metodo"
linktitle: "get_TintAndShade"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Border::get_TintAndShade metodo. Ottiene o imposta un valore double che schiarisce o scurisce un colore in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


Ottiene o imposta un valore double che schiarisce o scurisce un colore.

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## Note


I valori consentiti sono nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà. Zero (0) è neutro.

## Esempi



Mostra come inserire un paragrafo con un bordo superiore.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Imposta ThemeColor solo quando LineWidth o LineStyle sono impostati.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Vedi anche

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
