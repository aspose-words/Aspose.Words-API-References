---
title: "Aspose::Words::SectionCollection klass"
linktitle: "SectionCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::SectionCollection klass. En samling av Section-objekt i dokumentet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 59000
url: /sv/cpp/aspose.words/sectioncollection/
---
## SectionCollection class


En samling av [Section](../section/) objekt i dokumentet. För att lära dig mer, besök dokumentationsartikeln [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class SectionCollection : public Aspose::Words::NodeCollection
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Lägger till en nod i slutet av samlingen. |
| [Clear](../nodecollection/clear/)() | Tar bort alla noder från denna samling och från dokumentet. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Avgör om en nod finns i samlingen. |
| [get_Count](../nodecollection/get_count/)() | Hämtar antalet noder i samlingen. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Tillhandahåller en enkel "foreach"‑liknande iteration över samlingen av noder. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar ett avsnitt på det angivna indexet. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Infogar en nod i samlingen på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Tar bort noden på det angivna indexet från samlingen och från dokumentet. |
| [ToArray](./toarray/)() | Kopierar alla avsnitt från samlingen till en ny array av avsnitt. |
| static [Type](./type/)() |  |
## Anmärkningar


Ett Microsoft Word-dokument kan innehålla flera avsnitt. För att skapa ett avsnitt i Microsoft Word, välj kommandot Infoga/Avbrott och välj en avbrottstyp. Avbrottet anger om avsnittet startar på en ny sida eller på samma sida.

Att programatiskt infoga och ta bort avsnitt kan användas för att anpassa dokument som produceras under kopplad utskrift. Om ett dokument behöver ha olika innehåll eller delar av innehållet beroende på vissa kriterier, kan du skapa ett \"master\"-dokument som innehåller flera avsnitt och ta bort vissa avsnitt före eller efter kopplad utskrift.

## Exempel



Visar hur man lägger till och tar bort avsnitt i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Ta bort det första avsnittet från dokumentet.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Lägg till en kopia av det som nu är det första avsnittet i slutet av dokumentet.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Se även

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
