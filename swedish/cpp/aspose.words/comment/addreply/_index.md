---
title: "Aspose::Words::Comment::AddReply metod"
linktitle: "AddReply"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comment::AddReply metod. Lägger till ett svar på denna kommentar i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/comment/addreply/
---
## Comment::AddReply method


Lägger till ett svar på denna kommentar.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::AddReply(const System::String &author, const System::String &initial, System::DateTime dateTime, const System::String &text)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| författare | const System::String\& | Författarens namn för svaret. |
| initial | const System::String\& | Författarens initialer för svaret. |
| dateTime | System::DateTime | Datum och tid för svaret. |
| text | const System::String\& | Svarstexten. |

### ReturnValue

Den skapade [Comment](../) noden för svaret.
## Anmärkningar


På grund av befintliga MS Office-begränsningar tillåts endast 1 nivå av svar i dokumentet.

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
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
