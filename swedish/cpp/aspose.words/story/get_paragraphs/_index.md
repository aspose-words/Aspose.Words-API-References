---
title: "Aspose::Words::Story::get_Paragraphs metod"
linktitle: "get_Paragraphs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Story::get_Paragraphs metod. Hämtar en samling av stycken som är omedelbara barn till berättelsen i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/story/get_paragraphs/
---
## Story::get_Paragraphs method


Hämtar en samling stycken som är omedelbara barn till berättelsen.

```cpp
System::SharedPtr<Aspose::Words::ParagraphCollection> Aspose::Words::Story::get_Paragraphs() override
```


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

* Class [ParagraphCollection](../../paragraphcollection/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
