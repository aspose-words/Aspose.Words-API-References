---
title: "Aspose::Words::Comment::SetText metod"
linktitle: "SetText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comment::SetText metod. Detta är en bekvämlighetsmetod som gör det enkelt att ange texten för kommentaren i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words/comment/settext/
---
## Comment::SetText method


Detta är en bekvämlighetsmetod som möjliggör att enkelt ange texten för kommentaren.

```cpp
void Aspose::Words::Comment::SetText(const System::String &text)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| text | const System::String\& | Den nya texten för kommentaren. |
## Anmärkningar


Denna metod gör det möjligt att snabbt ange texten för en kommentar från en sträng. Strängen kan innehålla styckebrytningar, vilket kommer att skapa stycken med text i kommentaren enligt detta. Om du vill infoga mer komplexa element i kommentaren, till exempel bokmärken eller tabeller eller tillämpa rik formatering, måste du använda lämpliga nodklasser för att bygga upp kommentartexten.

## Exempel



Visar hur man lägger till en kommentar i ett dokument och sedan svarar på den.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Placera kommentaren på en nod i dokumentets kropp.
// Denna kommentar kommer att visas på platsen för dess stycke,
// utanför sidans högermarginal och med en prickad linje som förbinder den med dess stycke.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Lägg till ett svar, som kommer att visas under dess föräldrakommentar.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Kommentarer och svar är båda Comment-noder.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Kommentarer som inte svarar på andra kommentarer är "top-level". De har inga förfäderskommentarer.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Svar har en förfäderskommentar på toppnivå.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```

## Se även

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
