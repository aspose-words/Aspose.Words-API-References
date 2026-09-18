---
title: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade Methode"
linktitle: "get_ForeTintAndShade"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade Methode. Gibt einen double‑Wert zurück oder setzt ihn, der die Vordergrundfarbe des Strichs in C++ aufhellt oder abdunkelt."
type: docs
weight: 10667
url: /de/cpp/aspose.words.drawing/stroke/get_foretintandshade/
---
## Stroke::get_ForeTintAndShade method


Liest oder setzt einen double-Wert, der die Vordergrundfarbe des Strichs aufhellt oder abdunkelt.

```cpp
double Aspose::Words::Drawing::Stroke::get_ForeTintAndShade()
```

## Hinweise


Die zulässigen Werte liegen für diese Eigenschaft im Bereich von -1 (am dunkelsten) bis 1 (am hellsten). Null (0) ist neutral. Der Versuch, diese Eigenschaft auf einen Wert kleiner als -1 oder größer als 1 zu setzen, führt zu [ArgumentOutOfRangeException](../).

## Beispiele



Zeigt, wie man die Vordergrund‑Designfarbe sowie Farbton und Schattierung einstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## Siehe auch

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
