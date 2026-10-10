---
title: "Aspose::Words::ParagraphFormat::get_WidowControl metod"
linktitle: "get_WidowControl"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_WidowControl method. Sant om den första och sista raden i stycket ska förbli på samma sida som resten av stycket i C++."
type: docs
weight: 41000
url: /sv/cpp/aspose.words/paragraphformat/get_widowcontrol/
---
## ParagraphFormat::get_WidowControl method


Sant om den första och sista raden i stycket ska förbli på samma sida som resten av stycket.

```cpp
bool Aspose::Words::ParagraphFormat::get_WidowControl()
```


## Exempel



Visar hur man aktiverar kontroll av änkor och föräldralösa för ett stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// När vi skriver text som inte får plats på en sida kan en rad rinna över till nästa sida.
// Den enda raden som hamnar på nästa sida kallas en "Orphan",
// och den föregående raden där orphanen bröts av kallas en "Widow".
// Vi kan åtgärda föräldralösa och änkor genom att omarrangera text via teckenstorlek, avstånd eller sidmarginaler.
// Om vi vill bevara dokumentets dimensioner kan vi sätta denna flagga till "true"
// för att placera ensamrader på samma sida som deras respektive föräldralösa rader.
// Att lämna denna flagga som "false" kommer att lämna ensamrad/föräldralös par i texten.
// Varje stycke har denna inställning tillgänglig i Microsoft Word via Start -> Stycke -> Styckeinställningar
// (knapp i nedre högra hörnet av "Paragraph") -> "Widow/Orphan control".
builder->get_ParagraphFormat()->set_WidowControl(widowControl);

// Infoga text som skapar en föräldralös rad och en ensamrad.
builder->get_Font()->set_Size(68);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.WidowControl.docx");
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
