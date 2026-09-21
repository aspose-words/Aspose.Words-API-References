---
title: "Aspose::Words::Notes::Footnote::get_FootnoteType metod"
linktitle: "get_FootnoteType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::Footnote::get_FootnoteType metod. Returnerar ett värde som anger om detta är en fotnot eller slutnot i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.notes/footnote/get_footnotetype/
---
## Footnote::get_FootnoteType method


Returnerar ett värde som anger om detta är en fotnot eller en slutnot.

```cpp
Aspose::Words::Notes::FootnoteType Aspose::Words::Notes::Footnote::get_FootnoteType() const
```


## Exempel



Visar skillnaden mellan fotnoter och slutnoter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer två sätt att fästa numrerade referenser till texten. Båda dessa referenser kommer att lägga till en
// liten upphöjd referensmarkering på den plats där vi infogar dem.
// Referensmarkeringen är som standard indexnumret för referensen bland alla referenser i dokumentet.
// Varje referens kommer också att skapa en post, som kommer att ha samma referensmarkering som i brödtexten
// och referenstext, som vi kommer att skicka till dokumentbyggarens \"InsertFootnote\"-metod.
// 1 -  En fotnot, vars post kommer att visas på samma sida som den text den refererar till:
builder->Write(u"Footnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  En slutnot, vars post kommer att visas i slutet av dokumentet:
builder->Write(u"Endnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> endnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote text, will appear at the very end of the document.");

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Footnote, footnote->get_FootnoteType());
ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Endnote, endnote->get_FootnoteType());

doc->Save(get_ArtifactsDir() + u"InlineStory.FootnoteEndnote.docx");
```

## Se även

* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
