---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words för .NET
description: Rensa enkelt alla svar på din kommentar med metoden RemoveAllReplies, vilket säkerställer en rörig diskussion och en förbättrad användarupplevelse.
type: docs
weight: 170
url: /sv/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

Tar bort alla svar på den här kommentaren.

```csharp
public void RemoveAllReplies()
```

## Anmärkningar

Alla ingående noder i svaren kommer att raderas från dokumentet.

## Exempel

Visar hur man tar bort svar på kommentarer.

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// Nedan följer två sätt att ta bort svar från en kommentar.
// 1 - Använd metoden "RemoveReply" för att ta bort svar från en kommentar individuellt:
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 - Använd metoden "RemoveAllReplies" för att ta bort alla svar från en kommentar samtidigt:
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### Se även

* class [Comment](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
