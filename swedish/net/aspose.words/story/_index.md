---
title: Story Class
linktitle: Story
articleTitle: Story
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Story, ditt viktiga verktyg för att effektivt hantera element på blocknivå som stycken och tabeller.
type: docs
weight: 6960
url: /sv/net/aspose.words/story/
---
## Story class

Basklass för element som innehåller noder på blocknivå[`Paragraph`](../paragraph/) och[`Table`](../../aspose.words.tables/table/) .

För att lära dig mer, besök[Logiska nivåer av noder i ett dokument](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) dokumentationsartikel.

```csharp
public abstract class Story : CompositeNode
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Hämtar det första stycket i berättelsen. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Hämtar det sista stycket i berättelsen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Hämtar typen av denna nod. |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Hämtar en samling stycken som är direkta underordnade stycken till berättelsen. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Hämtar typen av den här berättelsen. |
| [Tables](../../aspose.words/story/tables/) { get; } | Hämtar en samling tabeller som är direkta underordnade tabeller till berättelsen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Tar emot en besökare. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | När den implementeras i en härledd klass, anropas VisitXXXEnd-metoden för den angivna dokumentbesökaren. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | När den implementeras i en härledd klass, anropas VisitXXXStart-metoden för den angivna dokumentbesökaren. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | En genvägsmetod som skapar en[`Paragraph`](../paragraph/) objekt med valfri text och lägger till den i slutet av detta objekt. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Tar bort alla former från texten i den här berättelsen. |
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
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Tar bort den angivna undernoden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underordnade noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../node/) som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

Text i ett Word-dokument sägs bestå av flera artiklar. Huvudtexten lagras i huvudtextartikeln som representeras av[`Body`](../body/) , varje sidhuvud och sidfot lagras i en separat artikel representerad av[`HeaderFooter`](../headerfooter/).

## Exempel

Visar hur man tar bort alla former från en nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en DocumentBuilder för att infoga en form. Detta är en inbäddad form,
// som har ett förälderparagraf, som är en undernod till den första sektionens brödtext.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Vi kan ta bort alla former från underparagraferna i denna brödtext.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Se även

* class [CompositeNode](../compositenode/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
