---
title: "Aspose::Words::Font::get_Kerning‑metod"
linktitle: "get_Kerning"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Kerning‑metod. Hämtar eller anger teckenstorleken då kerning startar i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words/font/get_kerning/
---
## Font::get_Kerning method


Hämtar eller anger teckensnittsstorleken då kerning påbörjas.

```cpp
double Aspose::Words::Font::get_Kerning()
```


## Exempel



Visar hur man anger teckenstorleken då kerning börjar träda i kraft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial Black");

// Ställ in byggarens teckenstorlek och minsta storlek då kerning ska börja gälla.
// Teckenstorleken faller under kerningströskeln, så körsegmentet nedan kommer inte att ha kerning.
builder->get_Font()->set_Size(18);
builder->get_Font()->set_Kerning(24);

builder->Writeln(u"TALLY. (Kerning not applied)");

// Ställ in kerningströskeln så att byggarens aktuella teckenstorlek är över den.
// All text vi lägger till från och med nu kommer att ha kerning tillämpad. Avstånden mellan tecken
// kommer att justeras, vilket normalt resulterar i ett något mer estetiskt tilltalande körsegment.
builder->get_Font()->set_Kerning(12);

builder->Writeln(u"TALLY. (Kerning applied)");

doc->Save(get_ArtifactsDir() + u"Font.Kerning.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
