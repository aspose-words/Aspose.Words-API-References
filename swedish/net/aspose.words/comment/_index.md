---
title: Comment Class
linktitle: Comment
articleTitle: Comment
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Comment, ditt viktiga verktyg för att hantera kommentartext i dokument. Förbättra ditt arbetsflöde med sömlös integration!
type: docs
weight: 420
url: /sv/net/aspose.words/comment/
---
## Comment class

Representerar en behållare för texten i en kommentar.

För att lära dig mer, besök[Arbeta med kommentarer](https://docs.aspose.com/words/net/working-with-comments/) dokumentationsartikel.

```csharp
public sealed class Comment : InlineStory
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Comment](comment/#constructor)(*[DocumentBase](../documentbase/)*) | Initierar en ny instans av`Comment` klass. |
| [Comment](comment/#constructor_1)(*[DocumentBase](../documentbase/), string, string, DateTime*) | Initierar en ny instans av`Comment` klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Returnerar föräldern`Comment`objekt. Returnerar`null` för kommentarer på toppnivå. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Returnerar eller anger författarnamnet för en kommentar. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Hämtar datum och tid då kommentaren gjordes. |
| [DateTimeUtc](../../aspose.words/comment/datetimeutc/) { get; } | Hämtar UTC-datum och -tid då kommentaren gjordes. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Hämtar eller sätter en flagga som indikerar att kommentaren har markerats som klar. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Hämtar det första stycket i berättelsen. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Ger åtkomst till teckensnittsformateringen för ankartecknet i detta objekt. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| [Id](../../aspose.words/comment/id/) { get; set; } | Hämtar eller ställer in kommentaridentifieraren. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Returnerar eller anger initialerna för den användare som är associerad med en specifik kommentar. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Returnerar sant om det här objektet togs bort i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Returer`sann` om det här objektet flyttades (raderades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Returer`sann` om det här objektet flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Hämtar det sista stycket i berättelsen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | ReturerComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Hämtar en samling stycken som är direkta underordnade stycken till berättelsen. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } | Hämtar eller ställer in det överordnade kommentars-ID:t. Värdet är`-1` betyder att kommentaren inte har någon förälder. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Hämtar föräldern[`Paragraph`](../paragraph/) av denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Returnerar en samling av`Comment` objekt som är omedelbara underordnade till den angivna kommentaren. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | ReturerComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Hämtar en samling tabeller som är direkta underordnade tabeller till berättelsen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare för att besöka slutet av kommentaren. |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Accepterar en besökare för att besöka början av kommentaren. |
| [AddReply](../../aspose.words/comment/addreply/)(*string, string, DateTime, string*) | Lägger till ett svar på den här kommentaren. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Om det sista underordnade stycket inte är ett stycke skapas och läggs till ett tomt stycke. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Returnerar indexet för den angivna undernoden i undernodsmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder till den aktuella noden. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Tar bort alla svar på den här kommentaren. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Tar bort den angivna undernoden. |
| [RemoveReply](../../aspose.words/comment/removereply/)(*Comment*) | Tar bort det angivna svaret på den här kommentaren. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underordnade noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../node/) som matchar XPath-uttrycket. |
| [SetText](../../aspose.words/comment/settext/)(*string*) | Detta är en bekväm metod som gör det enkelt att ange kommentarens text. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

En kommentar är en anteckning som är förankrad i ett textområde eller en position i texten. En kommentar kan innehålla en godtycklig mängd innehåll på blocknivå.

Om en`Comment` objektet förekommer på egen hand, kommentaren är förankrad till positionen för`Comment` objekt.

För att förankra en kommentar till ett textområde krävs tre objekt:`Comment` , [`CommentRangeStart`](../commentrangestart/) och[`CommentRangeEnd`](../commentrangeend/) Alla tre objekten måste dela samma [`Id`](./id/) värde.

`Comment` är en inline-nivånod och kan bara vara underordnad[`Paragraph`](../paragraph/).

`Comment` kan innehålla[`Paragraph`](../paragraph/) och[`Table`](../../aspose.words.tables/table/) underordnade noder.

## Exempel

Visar hur man lägger till en kommentar i ett stycke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // I Microsoft Word kan vi högerklicka på den här kommentaren i dokumentets brödtext för att redigera den eller svara på den.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

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

* class [InlineStory](../inlinestory/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
