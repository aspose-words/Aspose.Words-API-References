---
title: "Aspose::Words::Paragraph::JoinRunsWithSameFormatting metod"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Paragraph::JoinRunsWithSameFormatting metod. Slår ihop körningar med samma formatering i stycket i C++."
type: docs
weight: 31000
url: /sv/cpp/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph::JoinRunsWithSameFormatting() method


Sammanfogar körningar med samma formatering i stycket.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting()
```


### ReturnValue

Antal sammanslagningar som utförts. När **N** intilliggande körningar sammanfogas räknas de som **N - 1** sammanslagningar.

## Exempel



Visar hur man förenklar stycken genom att slå ihop överflödiga körningar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga fyra körningar av text i stycket.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");
builder->Write(u"Run 3. ");
builder->Write(u"Run 4. ");

// Om vi öppnar detta dokument i Microsoft Word kommer stycket att se ut som en sömlös textkropp.
// Det kommer dock att bestå av fyra separata körningar med samma formatering. Fragmenterade stycken som detta
// kan uppstå när vi manuellt redigerar delar av ett stycke många gånger i Microsoft Word.
System::SharedPtr<Aspose::Words::Paragraph> para = builder->get_CurrentParagraph();

ASSERT_EQ(4, para->get_Runs()->get_Count());

// Ändra stilen på den sista körningen för att skilja den från de tre första.
para->get_Runs()->idx_get(3)->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Emphasis);

// Vi kan köra \"JoinRunsWithSameFormatting\"-metoden för att optimera dokumentets innehåll
// genom att slå ihop liknande körningar till en, vilket minskar deras totala antal.
// Denna metod returnerar också antalet körningar som metoden slog ihop.
// Dessa två sammanslagningar skedde för att kombinera Körning #1, #2 och #3,
// medan Run #4 lämnas ute eftersom den har en inkompatibel stil.
ASSERT_EQ(2, para->JoinRunsWithSameFormatting());

// Antalet kvarvarande körningar kommer att vara lika med det ursprungliga antalet
// minus antalet körningssammanfogningar som \"JoinRunsWithSameFormatting\"-metoden utförde.
ASSERT_EQ(2, para->get_Runs()->get_Count());
ASSERT_EQ(u"Run 1. Run 2. Run 3. ", para->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"Run 4. ", para->get_Runs()->idx_get(1)->get_Text());
```

## Se även

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) method


Sammanfogar körningar med samma formatering i stycket.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr<Aspose::Words::JoinRunsOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| options | const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\& | Ytterligare alternativ |

### ReturnValue

Antal sammanslagningar som utförts. När **N** intilliggande körningar sammanfogas räknas de som **N - 1** sammanslagningar.

## Exempel



Visar hur man slår samman körningar med samma formatering samtidigt som man ignorerar överflödiga och obetydliga attribut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa körningar med identisk synlig formatering men vissa interna skillnader.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Verifiera körningar innan sammanslagning.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Konfigurera alternativ för att ignorera redundanta och obetydliga attribut under sammanslagning.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Ignorera redundanta körningsegenskaper som inte påverkar utseendet.
options->set_IgnoreInsignificant(true);
// Ignorera obetydliga skillnader som körningar som bara innehåller blanksteg.

// Slå samman körningar som har samma synliga formatering med hjälp av de utökade alternativen.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Verifiera att körningarna har slagits samman framgångsrikt.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## Se även

* Class [JoinRunsOptions](../../joinrunsoptions/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
