---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words för .NET
description: Förbättra dina diskussioner med metoden Kommentar- och svarsfunktion – lägg enkelt till svar på kommentarer och förbättra engagemanget på din plattform!
type: docs
weight: 160
url: /sv/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Lägger till ett svar på den här kommentaren.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| author | String | Författarnamnet för svaret. |
| initial | String | Författarens initialer för svaret. |
| dateTime | DateTime | Datum och tid för svaret. |
| text | String | Svarstexten. |

### Returvärde

Det skapade[`Comment`](../) nod för svaret.

### Undantag

| undantag | skick |
| --- | --- |
| InvalidOperationException | Utlöser om den här metoden anropas på den befintliga svarskommentaren. |

## Anmärkningar

På grund av befintliga begränsningar i MS Office är endast en svarsnivå tillåten i dokumentet.

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
