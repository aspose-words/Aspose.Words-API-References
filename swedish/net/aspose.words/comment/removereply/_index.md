---
title: Comment.RemoveReply
linktitle: RemoveReply
articleTitle: RemoveReply
second_title: Aspose.Words för .NET
description: Comment RemoveReply metod. Tar bort det angivna svaret på denna kommentar i C#.
type: docs
weight: 140
url: /sv/net/aspose.words/comment/removereply/
---
## Comment.RemoveReply method

Tar bort det angivna svaret på denna kommentar.

```csharp
public void RemoveReply(Comment reply)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| reply | Comment | Kommentarnoden för det raderande svaret. |

## Anmärkningar

Alla ingående noder i svaret kommer att raderas från dokumentet.

## Exempel

Visar hur man tar bort kommentarsvar.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count()); 

// Nedan finns två sätt att ta bort svar från en kommentar.
// 1 - Använd metoden "RemoveReply" för att ta bort svar från en kommentar individuellt:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count());

// 2 - Använd metoden "RemoveAllReplies" för att ta bort alla svar från en kommentar på en gång:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count());
```

### Se även

* class [Comment](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
