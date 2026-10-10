---
title: "Metodo Aspose::Words::Drawing::Fill::get_ForeTintAndShade"
linktitle: "get_ForeTintAndShade"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Fill::get_ForeTintAndShade. Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.drawing/fill/get_foretintandshade/
---
## Fill::get_ForeTintAndShade method


Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano.

```cpp
double Aspose::Words::Drawing::Fill::get_ForeTintAndShade()
```

## Note


I valori consentiti sono nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà.

Zero (0) è neutro.

## Esempi



Mostra come gestire lo schiarimento e l'oscuramento del colore del carattere di primo piano.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::Drawing::Fill> textFill = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Fill();
textFill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
if (textFill->get_ForeTintAndShade() == 0)
{
    textFill->set_ForeTintAndShade(0.5);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillTintAndShade.docx");
```

## Vedi anche

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
