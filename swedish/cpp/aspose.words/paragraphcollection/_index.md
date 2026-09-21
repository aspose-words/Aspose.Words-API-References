---
title: "Aspose::Words::ParagraphCollection-klass"
linktitle: "ParagraphCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphCollection-klass. Tillhandahåller typad åtkomst till en samling av Paragraph-noder. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 48000
url: /sv/cpp/aspose.words/paragraphcollection/
---
## ParagraphCollection class


Tillhandahåller typad åtkomst till en samling av [Paragraph](../paragraph/)-noder. För att lära dig mer, besök dokumentationsartikeln [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Hämtar en [Paragraph](../paragraph/) på det angivna indexet. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Infogar en nod i samlingen på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Tar bort noden på det angivna indexet från samlingen och från dokumentet. |
| [ToArray](./toarray/)() | Kopierar alla stycken från samlingen till en ny array av stycken. |
| static [Type](./type/)() |  |

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

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
