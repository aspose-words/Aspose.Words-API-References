---
title: "Aspose::Words::RunCollection::ToArray metod"
linktitle: "ToArray"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::RunCollection::ToArray metod. Kopierar alla runs från samlingen till en ny array av runs i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/runcollection/toarray/
---
## RunCollection::ToArray method


Kopierar alla run från samlingen till en ny array av run.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Run>> Aspose::Words::RunCollection::ToArray()
```


### ReturnValue

En array av runs.

## Exempel



Visar hur man bestämmer revideringstypen för en inline-nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// När vi redigerar dokumentet medan alternativet "Track Changes", som finns via Review -> Tracking,
// är aktiverat i Microsoft Word, räknas de ändringar vi gör som revideringar.
// När vi redigerar ett dokument med Aspose.Words kan vi börja spåra revideringar genom att
// anropa dokumentets "StartTrackRevisions"-metod och stoppa spårning genom att använda "StopTrackRevisions"-metoden.
// Vi kan antingen acceptera revisioner för att assimilera dem i dokumentet
// eller avvisa dem för att ändra den föreslagna ändringen effektivt.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Den överordnade noden för en revision är körningen som revisionen gäller. En Run är en Inline-nod.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Nedan är fem typer av revisioner som kan flagga en Inline-nod.
// 1 -  En "insert"-revision:
// Denna revision uppstår när vi infogar text medan vi spårar ändringar.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  En "format"-revision:
// Denna revision uppstår när vi ändrar formateringen av text medan vi spårar ändringar.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  En "move from"-revision:
// När vi markerar text i Microsoft Word och sedan drar den till en annan plats i dokumentet
// medan vi spårar ändringar visas två revisioner.
// "move from"-revisionen är en kopia av texten som ursprungligen fanns innan vi flyttade den.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  En "move to"-revision:
// "move to"-revisionen är texten som vi flyttade till sin nya position i dokumentet.
// "Move from"- och "move to"-revisioner visas i par för varje flyttrevision vi utför.
// Att acceptera en flyttrevision tar bort "move from"-revisionen och dess text,
// och behåller texten från "move to"-revisionen.
// Att avvisa en flyttrevision behåller däremot "move from"-revisionen och tar bort "move to"-revisionen.
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  En "delete"-revision:
// Denna revision uppstår när vi tar bort text medan vi spårar ändringar. När vi tar bort text på detta sätt,
// kommer den att finnas kvar i dokumentet som en revision tills vi antingen accepterar revisionen,
// vilket kommer att ta bort texten permanent, eller avvisar revisionen, vilket behåller den text vi tog bort på sin plats.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Se även

* Class [Run](../../run/)
* Class [RunCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
