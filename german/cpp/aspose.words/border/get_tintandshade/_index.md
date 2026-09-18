---
title: "Aspose::Words::Border::get_TintAndShade Methode"
linktitle: "get_TintAndShade"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border::get_TintAndShade Methode. Gibt einen double-Wert zurück oder legt ihn fest, der eine Farbe aufhellt oder abdunkelt in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


Liest oder setzt einen Double-Wert, der eine Farbe aufhellt oder abdunkelt.

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## Hinweise


Die zulässigen Werte liegen im Bereich von -1 (am dunkelsten) bis 1 (am hellsten) für diese Eigenschaft. Null (0) ist neutral.

## Beispiele



Zeigt, wie man einen Absatz mit einem oberen Rand einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Setze ThemeColor nur, wenn LineWidth oder LineStyle gesetzt ist.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Siehe auch

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
