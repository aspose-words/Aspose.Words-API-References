---
title: "Aspose::Words::Font::get_AutoColor metod"
linktitle: "get_AutoColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_AutoColor metod. Returnerar den aktuella beräknade färgen på texten (svart eller vit) som ska användas för ''auto color''. Om färgen inte är ''auto'' returneras Color i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/font/get_autocolor/
---
## Font::get_AutoColor method


Returnerar den aktuella beräknade färgen på texten (svart eller vit) som ska användas för 'auto color'. Om färgen inte är 'auto' returneras [Color](../get_color/).

```cpp
System::Drawing::Color Aspose::Words::Font::get_AutoColor()
```

## Anmärkningar


När text har 'automatic color' beräknas den faktiska färgen på texten automatiskt så att den är läsbar mot bakgrundsfärgen. När du ändrar bakgrundsfärgen byts textfärgen automatiskt till svart eller vitt i MS Word för att maximera läsbarheten.

## Exempel



Visar hur man förbättrar läsbarheten genom att automatiskt välja textfärg baserat på bakgrundens ljusstyrka.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Om ett runs Font‑objekt inte specificerar textfärg, kommer det automatiskt
// att välja antingen svart eller vitt beroende på bakgrundens färg.
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());

// Standardfärgen för text är svart. Om bakgrundens färg är mörk blir svart text svår att se.
// För att lösa detta problem kommer AutoColor-egenskapen att visa denna text i vitt.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"The text color automatically chosen for this run is white.");

ASSERT_EQ(System::Drawing::Color::get_White().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

// Om vi ändrar bakgrunden till en ljus färg, blir svart en mer
// lämplig textfärg än vit så att auto-färgen visar den i svart.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());

builder->Writeln(u"The text color automatically chosen for this run is black.");

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

doc->Save(get_ArtifactsDir() + u"Font.SetFontAutoColor.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
