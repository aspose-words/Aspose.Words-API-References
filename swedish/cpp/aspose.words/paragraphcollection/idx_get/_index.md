---
title: "Aspose::Words::ParagraphCollection::idx_get metod"
linktitle: "idx_get"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphCollection::idx_get metod. Hämtar ett Paragraph på det angivna indexet i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/paragraphcollection/idx_get/
---
## ParagraphCollection::idx_get method


Hämtar ett [Paragraph](../../paragraph/) på det angivna indexet.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::ParagraphCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Ett index i samlingen. |
## Anmärkningar


Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst sista och så vidare.

Om index är större än eller lika med antalet objekt i listan, returneras en null-referens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan, returneras en null-referens.

## Exempel



Visar hur man kontrollerar om ett stycke är en flyttrevision.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Det här dokumentet innehåller "Move"-revisioner, som visas när vi markerar text med markören,
// och sedan drar vi den för att flytta den till en annan plats
// medan vi spårar revisioner i Microsoft Word via "Review" -> "Track changes".
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Flyttrevisioner består av par av "Move from"- och "Move to"-revisioner.
// Dessa revisioner är potentiella ändringar i dokumentet som vi kan antingen acceptera eller avvisa.
// Innan vi accepterar/avvisar en flyttrevision, dokumentet
// måste hålla reda på både avrese- och ankomstdestinationerna för texten.
// Det andra och det fjärde stycket definierar en sådan revision, och därför har båda samma innehåll.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// "Move from"-revisionen är stycket där vi drog texten från.
// Om vi accepterar revisionen, kommer detta stycke att försvinna,
// och det andra kommer att kvarstå och inte längre vara en revision.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// Den "Move to"-revisionen är det stycke där vi drog texten till.
// Om vi avvisar revisionen kommer detta stycke istället att försvinna, och det andra att förbli.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## Se även

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
