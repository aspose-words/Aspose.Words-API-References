---
title: "Aspose::Words::InlineStory::get_IsDeleteRevision metod"
linktitle: "get_IsDeleteRevision"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::InlineStory::get_IsDeleteRevision metod. Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/inlinestory/get_isdeleterevision/
---
## InlineStory::get_IsDeleteRevision method


Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad.

```cpp
bool Aspose::Words::InlineStory::get_IsDeleteRevision()
```


## Exempel



Visar hur man visar revisionsrelaterade egenskaper för [InlineStory](../) noder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision footnotes.docx");

// När vi redigerar dokumentet medan alternativet "Track Changes", som finns via Review -> Tracking,
// är aktiverat i Microsoft Word, räknas de ändringar vi gör som revideringar.
// När vi redigerar ett dokument med Aspose.Words kan vi börja spåra revideringar genom att
// anropa dokumentets "StartTrackRevisions"-metod och stoppa spårning genom att använda "StopTrackRevisions"-metoden.
// Vi kan antingen acceptera revisioner för att assimilera dem i dokumentet
// eller avvisa dem för att ångra och kassera den föreslagna ändringen.
ASSERT_TRUE(doc->get_HasRevisions());

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Notes::Footnote>>> footnotes = doc->GetChildNodes(Aspose::Words::NodeType::Footnote, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Notes::Footnote> >()->LINQ_ToList();

ASSERT_EQ(5, footnotes->get_Count());

// Nedan följer fem typer av revisioner som kan flagga en InlineStory-nod.
// 1 -  En "insert"-revision:
// Denna revision uppstår när vi infogar text medan vi spårar ändringar.
ASSERT_TRUE(footnotes->idx_get(2)->get_IsInsertRevision());

// 2 -  En "move from"-revision:
// När vi markerar text i Microsoft Word och sedan drar den till en annan plats i dokumentet
// medan vi spårar ändringar visas två revisioner.
// "move from"-revisionen är en kopia av texten som ursprungligen fanns innan vi flyttade den.
ASSERT_TRUE(footnotes->idx_get(4)->get_IsMoveFromRevision());

// 3 -  En "move to"-revision:
// "move to"-revisionen är texten som vi flyttade till sin nya position i dokumentet.
// "Move from"- och "move to"-revisioner visas i par för varje flyttrevision vi utför.
// Att acceptera en flyttrevision tar bort "move from"-revisionen och dess text,
// och behåller texten från "move to"-revisionen.
// Att avvisa en flyttrevision behåller däremot "move from"-revisionen och tar bort "move to"-revisionen.
ASSERT_TRUE(footnotes->idx_get(1)->get_IsMoveToRevision());

// 4 -  En "delete"-revision:
// Denna revision uppstår när vi tar bort text medan vi spårar ändringar. När vi tar bort text på detta sätt,
// kommer den att finnas kvar i dokumentet som en revision tills vi antingen accepterar revisionen,
// vilket kommer att ta bort texten permanent, eller avvisar revisionen, vilket behåller den text vi tog bort på sin plats.
ASSERT_TRUE(footnotes->idx_get(3)->get_IsDeleteRevision());
```

## Se även

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
