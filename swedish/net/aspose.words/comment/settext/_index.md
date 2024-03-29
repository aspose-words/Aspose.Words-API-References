---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words för .NET
description: Comment SetText metod. Detta är en bekvämlighetsmetod som gör det enkelt att ställa in texten i kommentaren i C#.
type: docs
weight: 150
url: /sv/net/aspose.words/comment/settext/
---
## Comment.SetText method

Detta är en bekvämlighetsmetod som gör det enkelt att ställa in texten i kommentaren.

```csharp
public void SetText(string text)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| text | String | Den nya texten i kommentaren. |

## Anmärkningar

Denna metod gör det möjligt att snabbt ställa in text i en kommentar från en sträng. Strängen kan innehålla styckebrytningar, detta kommer att skapa textstycken i kommentaren i enlighet därmed. Om du vill infoga mer komplexa element i kommentaren, till exempel bookmarks eller tabeller eller tillämpa rik formatering, måste du använda lämpliga nodklasser att bygga upp kommentarstexten.

## Exempel

Visar hur man lägger till en kommentar till ett dokument och sedan svarar på det.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Placera kommentaren vid en nod i dokumentets brödtext.
// Den här kommentaren kommer att dyka upp på platsen för dess stycke,
// utanför sidans högra marginal och med en prickad linje som förbinder den med dess stycke.
builder.CurrentParagraph.AppendChild(comment);

// Lägg till ett svar, som kommer att dyka upp under dess överordnade kommentar.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Kommentarer och svar är båda Kommentarsnoder.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Kommentarer som inte svarar på andra kommentarer är "toppnivå". De har inga förfäders kommentarer.
Assert.Null(comment.Ancestor);

// Svaren har en kommentar på översta nivån.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Se även

* class [Comment](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
