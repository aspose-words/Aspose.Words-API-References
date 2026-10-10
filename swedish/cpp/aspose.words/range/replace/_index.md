---
title: "Aspose::Words::Range::Replace metod"
linktitle: "Ersätt"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Range::Replace metod. Ersätter alla förekomster av ett teckenmönster som specificeras av ett reguljärt uttryck med en annan sträng i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/range/replace/
---
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Ersätter alla förekomster av ett teckenmönster specificerat med ett reguljärt uttryck med en annan sträng.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Ersätter hela matchen som fångas av det reguljära uttrycket.

Metoden kan bearbeta radbrytningar i både mönster- och ersättningssträngar.

Du bör använda speciella metatecken om du behöver arbeta med radbrytningar:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Exempel



Visar hur man ersätter alla förekomster av ett reguljärt uttrycksmönster med annan text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"I decided to get the curtains in gray, ideal for the grey-accented room.");

doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"gr(a|e)y"), u"lavender");

ASSERT_EQ(u"I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc->GetText().Trim());
```

## Se även

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersätter alla förekomster av ett teckenmönster specificerat med ett reguljärt uttryck med en annan sträng.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| mönster | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Ett reguljärt uttrycksmönster som används för att hitta matchningar. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objekt för att specificera ytterligare alternativ. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Ersätter hela matchen som fångas av det reguljära uttrycket.

Metoden kan bearbeta radbrytningar i både mönster- och ersättningssträngar.

Du bör använda speciella metatecken om du behöver arbeta med radbrytningar:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Se även

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&) method


Ersätter alla förekomster av ett specificerat teckensträngsmönster med en ersättningssträng.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Mönstret kommer inte att användas som reguljärt uttryck. Vänligen använd [Replace()](../) om du behöver reguljära uttryck.

Används skiftlägesokänslig jämförelse.

Metoden kan bearbeta radbrytningar i både mönster- och ersättningssträngar.

Du bör använda speciella metatecken om du behöver arbeta med radbrytningar:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Exempel



Visar hur man utför en sök‑och‑ersätt‑textoperation på innehållet i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Greetings, _FullName_!");

// Utför en sök‑och‑ersätt‑operation på vårt dokuments innehåll och verifiera antalet ersättningar som genomfördes.
int32_t replacementCount = doc->get_Range()->Replace(u"_FullName_", u"John Doe");

ASSERT_EQ(1, replacementCount);
ASSERT_EQ(u"Greetings, John Doe!", doc->GetText().Trim());
```


Visar hur man lägger till formatering i stycken där en sök‑och‑ersätt‑operation har hittat matchningar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// Vi kan använda ett "FindReplaceOptions"‑objekt för att modifiera sök‑och‑ersätt‑processen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Ställ in egenskapen "Alignment" till "ParagraphAlignment.Right" för att högerjustera varje stycke
// som innehåller en matchning som sök‑och‑ersätt‑operationen hittar.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Ersätt varje punkt som står precis före ett styckebrott med ett utropstecken.
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## Se även

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Ersätter alla förekomster av ett specificerat teckensträngsmönster med en ersättningssträng.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| mönster | const System::String\& | En sträng som ska ersättas. |
| ersättning | const System::String\& | En sträng för att ersätta alla förekomster av mönster. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objekt för att specificera ytterligare alternativ. |

### ReturnValue

Antalet utförda ersättningar.
## Anmärkningar


Mönstret kommer inte att användas som reguljärt uttryck. Vänligen använd [Replace()](../) om du behöver reguljära uttryck.

Metoden kan bearbeta radbrytningar i både mönster- och ersättningssträngar.

Du bör använda speciella metatecken om du behöver arbeta med radbrytningar:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Exempel



Visar hur man ersätter text i ett dokuments sidfot.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```


Visar hur man växlar skiftlägeskänslighet vid en sök‑och‑ersätt‑operation.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Vi kan använda ett "FindReplaceOptions"‑objekt för att modifiera sök‑och‑ersätt‑processen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Ställ in flaggan "MatchCase" till "true" för att tillämpa skiftlägeskänslighet när du söker efter strängar att ersätta.
// Ställ in flaggan "MatchCase" till "false" för att ignorera teckenkänslighet när du söker efter text att ersätta.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Visar hur man växlar fristående ord‑endast sök‑och‑ersätt‑operationer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Vi kan använda ett "FindReplaceOptions"‑objekt för att modifiera sök‑och‑ersätt‑processen.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Ställ in flaggan "FindWholeWordsOnly" till "true" för att ersätta den hittade texten om den inte är en del av ett annat ord.
// Ställ in flaggan "FindWholeWordsOnly" till "false" för att ersätta all text oavsett dess omgivning.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```


Visar hur man ersätter alla förekomster av en textsträng i en tabell och cell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Carrots");
builder->InsertCell();
builder->Write(u"50");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Potatoes");
builder->InsertCell();
builder->Write(u"50");
builder->EndTable();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(true);
options->set_FindWholeWordsOnly(true);

// Utför en sök‑och‑ersätt‑operation på en hel tabell.
table->get_Range()->Replace(u"Carrots", u"Eggs", options);

// Utför en sök‑och‑ersätt‑operation på den sista cellen i den sista raden i tabellen.
table->get_LastRow()->get_LastCell()->get_Range()->Replace(u"50", u"20", options);

ASSERT_EQ(System::String(u"Eggs\a50\a\a") + u"Potatoes\a20\a\a", table->GetText().Trim());
```

## Se även

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
