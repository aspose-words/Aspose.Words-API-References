---
title: "Aspose::Words::ParagraphFormat::get_LineSpacing metod"
linktitle: "get_LineSpacing"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_LineSpacing metod. Hämtar eller anger radavståndet (i punkter) för stycket i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words/paragraphformat/get_linespacing/
---
## ParagraphFormat::get_LineSpacing method


Hämtar eller anger radavståndet (i punkter) för stycket.

```cpp
double Aspose::Words::ParagraphFormat::get_LineSpacing()
```

## Anmärkningar


När egenskapen [LineSpacingRule](../get_linespacingrule/) är inställd på [AtLeast](../../linespacingrule/), kan radavståndet vara större än eller lika med, men aldrig mindre än det angivna värdet för [LineSpacing](./).

När egenskapen [LineSpacingRule](../get_linespacingrule/) är inställd på [Exactly](../../linespacingrule/), ändras radavståndet aldrig från det angivna värdet för [LineSpacing](./), även om ett större teckensnitt används i stycket.

## Exempel



Visar hur man arbetar med radavstånd.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer tre radavståndsregler som vi kan definiera med hjälp av
// styckets "LineSpacingRule"-egenskap för att konfigurera avståndet mellan stycken.
// 1 -  Ställ in ett minsta avstånd av mellanrum.
// Detta ger vertikal utfyllnad till textrader av vilken storlek som helst
// som är för liten för att upprätthålla minsta radavstånd.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::AtLeast);
builder->get_ParagraphFormat()->set_LineSpacing(20);

builder->Writeln(u"Minimum line spacing of 20.");
builder->Writeln(u"Minimum line spacing of 20.");

// 2 -  Ställ in exakt avstånd.
// Att använda teckenstorlekar som är för stora för avståndet kommer att trunkera texten.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Exactly);
builder->get_ParagraphFormat()->set_LineSpacing(5);

builder->Writeln(u"Line spacing of exactly 5.");
builder->Writeln(u"Line spacing of exactly 5.");

// 3 -  Ställ in avstånd som en multipel av standardradavstånd, som är 12 punkter som standard.
// Denna typ av avstånd kommer att skalas till olika teckenstorlekar.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Multiple);
builder->get_ParagraphFormat()->set_LineSpacing(18);

builder->Writeln(u"Line spacing of 1.5 default lines.");
builder->Writeln(u"Line spacing of 1.5 default lines.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LineSpacing.docx");
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
