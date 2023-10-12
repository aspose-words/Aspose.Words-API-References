---
title: Class Comment
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Comment klass. Representerar en behållare för text i en kommentar.
type: docs
weight: 230
url: /sv/net/aspose.words/comment/
---
## Comment class

Representerar en behållare för text i en kommentar.

För att lära dig mer, besök[Arbeta med kommentarer](https://docs.aspose.com/words/net/working-with-comments/) dokumentationsartikel.

```csharp
public sealed class Comment : InlineStory
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [Comment](comment/#constructor)(DocumentBase) | Initierar en ny instans av`Comment` class. |
| [Comment](comment/#constructor_1)(DocumentBase, string, string, DateTime) | Initierar en ny instans av`Comment` class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Returnerar den överordnade`Comment` objekt. Returnerar`null` för kommentarer på toppnivå. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Returnerar eller ställer in författarens namn för en kommentar. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Hämtar datum och tid då kommentaren gjordes. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Hämtar eller sätter en flagga som indikerar att kommentaren har markerats som klar. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Får det första barnet i noden. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Får första stycket i berättelsen. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Ger tillgång till teckensnittsformateringen av ankartecknet för detta objekt. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returnerar`Sann` om denna nod har några undernoder. |
| [Id](../../aspose.words/comment/id/) { get; set; } | Hämtar kommentarsidentifieraren. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Returnerar eller ställer in initialerna för användaren som är kopplad till en specifik kommentar. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returnerar`Sann` eftersom denna nod kan ha underordnade noder. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Returnerar sant om detta objekt raderades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Returnerar`Sann` om det här objektet flyttades (borttogs) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Returnerar`Sann` om detta objekt flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista underordnade. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Hämtar det sista stycket i berättelsen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | ReturnerarComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Får en samling stycken som är omedelbara barn till berättelsen. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Hämtar föräldern[`Paragraph`](../paragraph/) av denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/) objekt som representerar den del av ett dokument som finns i denna nod. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Returnerar en samling av`Comment` objekt som är omedelbara underordnade av den angivna kommentaren. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | ReturnerarComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Får en samling tabeller som är omedelbara barn till berättelsen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(DocumentVisitor) | Accepterar en besökare. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(DocumentVisitor) |  |
| [AddReply](../../aspose.words/comment/addreply/)(string, string, DateTime, string) | Lägger till ett svar på den här kommentaren. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar navigator som kan användas för att korsa och läsa noder. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Om det sista underordnade inte är ett stycke, skapar och lägger till ett tomt stycke. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Tar bort alla svar på den här kommentaren. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveReply](../../aspose.words/comment/removereply/)(Comment) | Tar bort det angivna svaret på denna kommentar. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/)underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Väljer den första[`Node`](../node/) som matchar XPath-uttrycket. |
| [SetText](../../aspose.words/comment/settext/)(string) | Detta är en bekvämlighetsmetod som gör det enkelt att ställa in texten i kommentaren. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

En kommentar är en anteckning som är förankrad till ett textområde eller till en position i text. En kommentar kan innehålla en godtycklig mängd innehåll på blocknivå.

Om en`Comment` objektet uppstår av sig självt, är kommentaren förankrad till positionen för`Comment` objekt.

För att förankra en kommentar till en textregion krävs tre objekt:`Comment` , [`CommentRangeStart`](../commentrangestart/) och[`CommentRangeEnd`](../commentrangeend/) . Alla tre objekt måste dela same [`Id`](./id/) värde.

`Comment` är en nod på inline-nivå och kan bara vara ett barn till[`Paragraph`](../paragraph/).

`Comment` kan innehålla[`Paragraph`](../paragraph/) och[`Table`](../../aspose.words.tables/table/) barnnoder.

### Exempel

Visar hur man lägger till en kommentar till ett stycke.

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

* class [InlineStory](../inlinestory/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


