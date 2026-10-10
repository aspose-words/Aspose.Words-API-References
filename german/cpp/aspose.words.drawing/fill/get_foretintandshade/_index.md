---
title: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade-Methode"
linktitle: "get_ForeTintAndShade"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade-Methode. Gibt einen double‑Wert zurück oder setzt ihn, der die Vordergrundfarbe in C++ aufhellt oder abdunkelt."
type: docs
weight: 9000
url: /de/cpp/aspose.words.drawing/fill/get_foretintandshade/
---
## Fill::get_ForeTintAndShade method


Liest oder legt einen double-Wert fest, der die Vordergrundfarbe aufhellt oder abdunkelt.

```cpp
double Aspose::Words::Drawing::Fill::get_ForeTintAndShade()
```

## Hinweise


Die zulässigen Werte liegen im Bereich von -1 (am dunkelsten) bis 1 (am hellsten) für diese Eigenschaft.

Null (0) ist neutral.

## Beispiele



Zeigt, wie man das Aufhellen und Abdunkeln der Vordergrund‑Schriftfarbe verwaltet.
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

## Siehe auch

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
