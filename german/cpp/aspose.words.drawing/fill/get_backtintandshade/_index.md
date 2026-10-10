---
title: "Aspose::Words::Drawing::Fill::get_BackTintAndShade-Methode"
linktitle: "get_BackTintAndShade"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Fill::get_BackTintAndShade-Methode. Ruft einen double-Wert ab oder legt ihn fest, der die Hintergrundfarbe aufhellt oder abdunkelt in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing/fill/get_backtintandshade/
---
## Fill::get_BackTintAndShade method


Liest oder legt einen double-Wert fest, der die Hintergrundfarbe aufhellt oder abdunkelt.

```cpp
double Aspose::Words::Drawing::Fill::get_BackTintAndShade()
```

## Hinweise


Die zulässigen Werte liegen im Bereich von -1 (am dunkelsten) bis 1 (am hellsten) für diese Eigenschaft.

Null (0) ist neutral.

## Beispiele



Zeigt, wie man die Themenfarbe für Vorder-/Hintergrundformenfarbe festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// Hinweis: Verwenden Sie nicht "BackThemeColor" und "BackTintAndShade" für die Schriftfüllung.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## Siehe auch

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
