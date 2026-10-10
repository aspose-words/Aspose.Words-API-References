---
title: "Aspose::Words::Section::AppendContent metod"
linktitle: "AppendContent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Section::AppendContent metod. Infogar en kopia av innehållet från källavsnittet i slutet av detta avsnitt i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/section/appendcontent/
---
## Section::AppendContent method


Infogar en kopia av innehållet i källavsnittet i slutet av detta avsnitt.

```cpp
void Aspose::Words::Section::AppendContent(const System::SharedPtr<Aspose::Words::Section> &sourceSection)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sourceSection | const System::SharedPtr\<Aspose::Words::Section\>\& | Sektionen att kopiera innehåll från. |
## Anmärkningar


Endast innehållet i [Body](../get_body/) för källsektionen kopieras, sidinställningar, sidhuvuden och sidfötter kopieras inte.

Noderna importeras automatiskt om källsektionen tillhör ett annat dokument.

Ingen ny sektion skapas i destinationsdokumentet.

## Exempel



Visar hur man lägger till innehållet i en sektion till en annan sektion.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

System::SharedPtr<Aspose::Words::Section> section = doc->get_Sections()->idx_get(2);

ASSERT_EQ(System::String(u"Section 3") + Aspose::Words::ControlChar::SectionBreak(), section->GetText());

// Infoga innehållet i den första sektionen i början av den tredje sektionen.
System::SharedPtr<Aspose::Words::Section> sectionToPrepend = doc->get_Sections()->idx_get(0);
section->PrependContent(sectionToPrepend);

// Infoga innehållet i den andra sektionen i slutet av den tredje sektionen.
System::SharedPtr<Aspose::Words::Section> sectionToAppend = doc->get_Sections()->idx_get(1);
section->AppendContent(sectionToAppend);

// Metoderna "PrependContent" och "AppendContent" skapade inga nya sektioner.
ASSERT_EQ(3, doc->get_Sections()->get_Count());
ASSERT_EQ(System::String(u"Section 1") + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 3" + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 2" + Aspose::Words::ControlChar::SectionBreak(), section->GetText());
```

## Se även

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
