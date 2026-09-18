---
title: "Aspose::Words::Shading::get_ForegroundTintAndShade Methode"
linktitle: "get_ForegroundTintAndShade"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Shading::get_ForegroundTintAndShade Methode. Ruft einen double-Wert ab oder legt ihn fest, der eine Vordergrund-Theme-Farbe aufhellt oder abdunkelt in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/shading/get_foregroundtintandshade/
---
## Shading::get_ForegroundTintAndShade method


Liest oder legt fest einen double-Wert, der eine Vordergrund-Theme-Farbe aufhellt oder abdunkelt.

```cpp
double Aspose::Words::Shading::get_ForegroundTintAndShade()
```

## Hinweise


Die zulässigen Werte liegen im Bereich von -1 (am dunkelsten) bis 1 (am hellsten) für diese Eigenschaft.

Null (0) ist neutral.

## Beispiele



Zeigt, wie Vorder‑ und Hintergrundfarben für die Schattierungstextur festgelegt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Shading> shading = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::Texture12Pt5Percent);
shading->set_ForegroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
shading->set_BackgroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);

shading->set_ForegroundTintAndShade(0.5);
shading->set_BackgroundTintAndShade(-0.2);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Writeln(u"Foreground and background pattern colors for shading texture.");

doc->Save(get_ArtifactsDir() + u"Font.ForegroundAndBackground.docx");
```

## Siehe auch

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
