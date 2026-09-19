---
title: "Aspose::Words::Shading::get_ForegroundTintAndShade metodo"
linktitle: "get_ForegroundTintAndShade"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Shading::get_ForegroundTintAndShade metodo. Ottiene o imposta un valore double che schiarisce o scurisce il colore del tema di primo piano in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/shading/get_foregroundtintandshade/
---
## Shading::get_ForegroundTintAndShade method


Ottiene o imposta un valore double che schiarisce o scurisce un colore tematico di primo piano.

```cpp
double Aspose::Words::Shading::get_ForegroundTintAndShade()
```

## Note


I valori consentiti sono nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà.

Zero (0) è neutro.

## Esempi



Mostra come impostare i colori di primo piano e di sfondo per la texture di shading.
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

## Vedi anche

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
