---
title: CommentCollection.Item
second_title: Aspose.Words för .NET API Referens
description: CommentCollection fast egendom. Hämtar en Kommentar vid det givna indexet.
type: docs
weight: 10
url: /sv/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Hämtar en **Kommentar** vid det givna indexet.

```csharp
public Comment this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Ett index i samlingen. |

### Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från baksidan av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder näst före sist och så vidare.

Om index är större än eller lika med antalet objekt i listan, returnerar detta en nollreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan, returnerar detta en nollreferens.

### Exempel

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

* class [Comment](../../comment/)
* class [CommentCollection](../)
* namnutrymme [Aspose.Words](../../commentcollection/)
* hopsättning [Aspose.Words](../../../)


