---
title: "Aspose::Words::Drawing::Stroke::get_BackTintAndShade Methode"
linktitle: "get_BackTintAndShade"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Stroke::get_BackTintAndShade Methode. Ermittelt oder legt einen double-Wert fest, der die Hintergrundfarbe des Strichs aufhellt oder abdunkelt in C++."
type: docs
weight: 2334
url: /de/cpp/aspose.words.drawing/stroke/get_backtintandshade/
---
## Stroke::get_BackTintAndShade method


Ruft einen double-Wert ab oder legt ihn fest, der die Hintergrundfarbe des Strichs aufhellt oder abdunkelt.

```cpp
double Aspose::Words::Drawing::Stroke::get_BackTintAndShade()
```

## Hinweise


Die zulässigen Werte liegen für diese Eigenschaft im Bereich von -1 (am dunkelsten) bis 1 (am hellsten). Null (0) ist neutral. Der Versuch, diese Eigenschaft auf einen Wert kleiner als -1 oder größer als 1 zu setzen, führt zu [ArgumentOutOfRangeException](../).

## Beispiele



Zeigt, wie man die Hintergrund-Theme-Farbe sowie Tönung und Schattierung einstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## Siehe auch

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
