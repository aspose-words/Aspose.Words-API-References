---
title: Comment.AddReply
second_title: Aspose.Words för .NET API Referens
description: Comment metod. Lägger till ett svar på den här kommentaren.
type: docs
weight: 120
url: /sv/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Lägger till ett svar på den här kommentaren.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| author | String | Författarens namn för svaret. |
| initial | String | Författaren initialer för svaret. |
| dateTime | DateTime | Datum och tid för svaret. |
| text | String | Svarstexten. |

### Returvärde

Det skapade[`Comment`](../) nod för svaret.

### Anmärkningar

På grund av de befintliga MS Office-begränsningarna tillåts endast en nivå av svar i dokumentet. Ett undantag av typenInvalidOperationException kommer att höjas om denna metod anropas på den befintliga Svarskommentaren.

### Exempel

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
* namnutrymme [Aspose.Words](../../comment/)
* hopsättning [Aspose.Words](../../../)


