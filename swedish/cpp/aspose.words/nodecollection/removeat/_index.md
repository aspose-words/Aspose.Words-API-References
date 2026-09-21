---
title: "Aspose::Words::NodeCollection::RemoveAt‑metod"
linktitle: "RemoveAt"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeCollection::RemoveAt‑metod. Tar bort noden på det angivna indexet från samlingen och från dokumentet i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/nodecollection/removeat/
---
## NodeCollection::RemoveAt method


Tar bort noden på det angivna indexet från samlingen och från dokumentet.

```cpp
void Aspose::Words::NodeCollection::RemoveAt(int32_t index)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Det nollbaserade indexet för noden. Negativa index är tillåtna och indikerar åtkomst från listans slut. Till exempel betyder -1 den sista noden, -2 den näst sista och så vidare. |

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

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
