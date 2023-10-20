---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: Aspose.Words för .NET
description: Aspose.Words.CommentCollection klass. Ger maskinskriven åtkomst till en samling avComment noder i C#.
type: docs
weight: 240
url: /sv/net/aspose.words/commentcollection/
---
## CommentCollection class

Ger maskinskriven åtkomst till en samling av[`Comment`](../comment/) noder.

För att lära dig mer, besök[Arbeta med kommentarer](https://docs.aspose.com/words/net/working-with-comments/) dokumentationsartikel.

```csharp
public class CommentCollection : NodeCollection
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Hämtar antalet noder i samlingen. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Hämtar en[`Comment`](../comment/) vid det givna indexet. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Lägger till en nod i slutet av samlingen. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tar bort alla noder från den här samlingen och från dokumentet. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bestämmer om en nod finns i samlingen. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Ger en enkel "foreach" stil iteration över samlingen av noder. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Infogar en nod i samlingen vid det angivna indexet. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Tar bort noden vid det angivna indexet från samlingen och från dokumentet. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Kopierar alla noder från samlingen till en ny array av noder. |

## Exempel

Visar hur man markerar en kommentar som "klar".

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // Infoga en kommentar för att påpeka ett fel.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // Kommentarer har en "Klar"-flagga, som är inställd på "false" som standard.
// Om en kommentar antyder att vi gör en ändring i dokumentet,
// vi kan tillämpa ändringen, och sedan även sätta flaggan "Klar" efteråt för att indikera korrigeringen.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// Kommentarer som är "klara" kommer att skilja sig åt
// från sådana som inte är "klara" med en blek textfärg.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### Se även

* class [NodeCollection](../nodecollection/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
