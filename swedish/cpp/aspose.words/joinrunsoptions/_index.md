---
title: "Aspose::Words::JoinRunsOptions klass"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::JoinRunsOptions klass. Tillhandahåller konfigurationsflaggor för sammanslagningsoperationen i C++."
type: docs
weight: 38500
url: /sv/cpp/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class


Tillhandahåller konfigurationsflaggor för operationen att slå ihop körningar.

```cpp
class JoinRunsOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_IgnoreInsignificant](./get_ignoreinsignificant/)() const | True indikerar att de obetydliga attributen för alla körningar kommer att ignoreras när körningar med samma formatering slås samman. |
| [get_IgnoreRedundant](./get_ignoreredundant/)() const | True indikerar att de överflödiga attributen för alla körningar kommer att ignoreras när körningar med samma formatering slås samman. |
| [get_IgnoreSpacing](./get_ignorespacing/)() const | True indikerar att avståndsattributen för alla körningar kommer att ignoreras när körningar med samma formatering slås samman. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsOptions](./joinrunsoptions/)() |  |
| [set_IgnoreInsignificant](./set_ignoreinsignificant/)(bool) | True indikerar att de obetydliga attributen för alla körningar kommer att ignoreras när körningar med samma formatering slås samman. |
| [set_IgnoreRedundant](./set_ignoreredundant/)(bool) | True indikerar att de överflödiga attributen för alla körningar kommer att ignoreras när körningar med samma formatering slås samman. |
| [set_IgnoreSpacing](./set_ignorespacing/)(bool) | True indikerar att avståndsattributen för alla körningar kommer att ignoreras när körningar med samma formatering slås samman. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
