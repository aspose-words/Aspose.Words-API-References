---
title: CommentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkelt åtkomst till specifika kommentarer med egenskapen CommentCollection Item. Hämta kommentarer via index för effektiv innehållshantering.
type: docs
weight: 10
url: /sv/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

Hämtar en[`Comment`](../../comment/) vid det givna indexet.

```csharp
public Comment this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Ett index till samlingen. |

## Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst före sista och så vidare.

Om index är större än eller lika med antalet objekt i listan returnerar detta en nullreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan returnerar detta en null-referens.

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

* class [Comment](../../comment/)
* class [CommentCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
