---
title: DocumentBase Class
linktitle: DocumentBase
articleTitle: DocumentBase
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.DocumentBase, den viktiga grunden för att skapa och hantera Word-dokument och ordlistor med lätthet och effektivitet.
type: docs
weight: 650
url: /sv/net/aspose.words/documentbase/
---
## DocumentBase class

Tillhandahåller den abstrakta basklassen för ett huvuddokument och ett ordlistadokument i ett Word-dokument.

För att lära dig mer, besök[Aspose.Words-dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Hämtar eller ställer in dokumentets bakgrundsform. Kan vara`null` . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Hämtar denna instans. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Ger åtkomst till egenskaper för teckensnitt som används i detta dokument. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Ger åtkomst till fotnots-/slutnotsavgränsare som definierats i dokumentet. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Ger åtkomst till listformateringen som används i dokumentet. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Anropas när en nod infogas eller tas bort i dokumentet. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Hämtar typen av denna nod. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Hämtar eller ställer in dokumentets sidfärg. Den här egenskapen är en enklare version av[`BackgroundShape`](./backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Gör det möjligt att styra hur externa resurser laddas. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Returnerar en samling stilar definierade i dokumentet. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Anropas under olika dokumentbehandlingsprocedurer när ett problem upptäcks som kan resultera i förlust av data- eller formateringsåtergivning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Tar emot en besökare. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | När den implementeras i en härledd klass, anropas VisitXXXEnd-metoden för den angivna dokumentbesökaren. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | När den implementeras i en härledd klass, anropas VisitXXXStart-metoden för den angivna dokumentbesökaren. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode)(*[Node](../node/), bool*) | Importerar en nod från ett annat dokument till det aktuella dokumentet. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode_1)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formateringen. |
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

Aspose.Words representerar ett Word-dokument som ett träd av noder.`DocumentBase` är en rotnod i trädet som innehåller alla andra noder i dokumentet.

`DocumentBase` lagrar även dokumentomfattande information som t.ex.[`Styles`](./styles/) och [`Lists`](./lists/) som trädnoderna kan referera till.

## Exempel

Visar hur man initierar underklasserna i DocumentBase.

```csharp
Document doc = new Document();

Assert.AreEqual(typeof(DocumentBase), doc.GetType().BaseType);

GlossaryDocument glossaryDoc = new GlossaryDocument();
doc.GlossaryDocument = glossaryDoc;

Assert.AreEqual(typeof(DocumentBase), glossaryDoc.GetType().BaseType);
```

### Se även

* class [CompositeNode](../compositenode/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
