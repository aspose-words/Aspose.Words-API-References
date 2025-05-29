---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words för .NET
description: Upptäck SetText-metoden, ett användarvänligt verktyg som förenklar att lägga till kommentarer, förbättrar ditt arbetsflöde och ökar produktiviteten utan ansträngning.
type: docs
weight: 190
url: /sv/net/aspose.words/comment/settext/
---
## Comment.SetText method

Detta är en bekväm metod som gör det enkelt att ange kommentarens text.

```csharp
public void SetText(string text)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| text | String | Kommentarens nya text. |

## Anmärkningar

Den här metoden gör det möjligt att snabbt ställa in texten i en kommentar från en sträng. Strängen kan innehålla styckebrytningar, vilket skapar textstycken i kommentaren därefter. Om du vill infoga mer komplexa element i kommentaren, till exempel bokmärken eller tabeller, eller använda rik formatering, måste du använda lämpliga nodklasser för att bygga upp kommentartexten.

## Exempel

Visar hur man lägger till en kommentar i ett dokument och sedan svarar på den.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Placera kommentaren vid en nod i dokumentets brödtext.
// Den här kommentaren kommer att visas där stycket är placerat,
// utanför sidans högra marginal och med en prickad linje som förbinder den med sitt stycke.
builder.CurrentParagraph.AppendChild(comment);

// Lägg till ett svar, som visas under dess överordnade kommentar.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Kommentarer och svar är båda kommentarsnoder.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Kommentarer som inte svarar på andra kommentarer är "toppnivå". De har inga överordnade kommentarer.
Assert.Null(comment.Ancestor);

// Svar har en överordnad kommentar på toppnivå.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Se även

* class [Comment](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
