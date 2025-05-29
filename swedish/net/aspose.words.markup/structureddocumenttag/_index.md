---
title: StructuredDocumentTag Class
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Markup.StructuredDocumentTag-klassen för effektiv innehållskontroll i dokument. Förbättra din dokumenthantering med SDT-funktioner!
type: docs
weight: 4750
url: /sv/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Representerar en strukturerad dokumenttagg (SDT eller innehållskontroll) i ett dokument.

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/), [MarkupLevel](../markuplevel/)*) | Initierar en ny instans av**Tagg för strukturerat dokument** klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Hämtar/ställer in utseendet på en strukturerad dokumenttagg. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Anger kategori för byggsten för detta**SDT** nod. Kan inte vara`null` . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Anger typ av byggsten för detta**SDT** . Kan inte vara`null` . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Anger kalendertypen för detta**SDT** . Standard ärDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Hämtar/ställer in aktuellt tillstånd för kryssrutan**SDT** . Standardvärdet för den här egenskapen är`falsk` . |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Hämtar eller ställer in färgen på den strukturerade dokumenttaggen. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Teckensnittsformatering som kommer att tillämpas på text som matas in i**SDT** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | Sträng som representerar formatet i vilket datum visas. |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Gör det möjligt att ställa in/hämta språkformat för datumet som visas i detta**SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | Hämtar/ställer in formatet i vilket datumet för en datum-SDT lagras när**SDT** är bunden till en XML-nod i dokumentets datalager. Standardvärdet ärDateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Teckensnittsformatering som kommer att tillämpas på det sista tecknet i texten som matas in i**SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Anger det fullständiga datumet och den senast inmatade tiden i detta**SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Anger ett unikt skrivskyddat, beständigt numeriskt ID för detta**SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Anger om innehållet i detta**SDT** ska tolkas som att innehålla platshållartext (i motsats till vanligt textinnehåll inom SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Anger om detta**SDT** ska tas bort från WordProcessingML-dokumentet när dess innehåll ändras. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Hämtar nivån vid vilken detta**SDT** förekommer i dokumentträdet. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | Får[`SdtListItemCollection`](../sdtlistitemcollection/) i samband med detta**SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | När den är inställd på`sann` , kommer den här egenskapen att förhindra att en användare tar bort detta**SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | När den är inställd på`sann` , kommer den här egenskapen att förhindra att en användare redigerar innehållet i detta**SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Anger om detta**SDT** tillåter flera rader text. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | ReturerStructuredDocumentTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Hämtar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) innehåller platshållartext som ska visas när innehållet i denna SDT-körning är tomt, det associerade mappade XML-elementet är tomt enligt anvisningarna via[`XmlMapping`](./xmlmapping/) element eller[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) elementet är`sann` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Hämtar eller anger namnet på[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) innehåller platshållartext. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Hämtar typ av detta**Tagg för strukturerat dokument** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Hämtar eller ställer in stilen för den strukturerade dokumenttaggen. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Hämtar eller anger namnet på den stil som tillämpas på den strukturerade dokumenttaggen. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Anger en tagg som är associerad med den aktuella SDT-noden. Kan inte`null` . |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Anger det användarvänliga namnet som är associerat med detta**SDT** . Kan inte vara`null` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Hämtar en sträng som representerar XML-koden som finns i noden iFlatOpc format. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | Hämtar en sträng som representerar XML-koden som finns i noden iFlatOpc format. Till skillnad från[`WordOpenXML`](./wordopenxml/) egenskapen genererar den här metoden ett avskalat dokument som exkluderar alla delar som inte är innehållsrelaterade. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Hämtar ett objekt som representerar mappningen av denna strukturerade dokumenttagg till XML-data i en anpassad XML-del av det aktuella dokumentet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka slutet av StructuredDocumentTag. |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka början av StructuredDocumentTag. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Rensar innehållet i den här strukturerade dokumenttaggen och visar en platshållare om den är definierad. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Returnerar indexet för den angivna undernoden i undernodsmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder till den aktuella noden. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Tar bort den angivna undernoden. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Tar bort endast denna SDT-nod, men behåller dess innehåll i dokumentträdet. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../smarttag/) underordnade noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../../aspose.words/node/) som matchar XPath-uttrycket. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(*int, string*) | Anger symbolen som används för att representera det markerade tillståndet för en innehållskontroll för kryssrutor. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(*int, string*) | Anger symbolen som används för att representera det okontrollerade tillståndet för en innehållskontroll i kryssrutan. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

Strukturerade dokumenttaggar (SDT) gör det möjligt att bädda in kunddefinierad semantik samt dess beteende och utseende i ett dokument.

den här versionen tillhandahåller Aspose.Words ett antal publika metoder och egenskaper för att manipulera beteendet och innehållet hos`StructuredDocumentTag` . Mappning av SDT-noder till anpassade XML-paket i ett dokument kan utföras med hjälp av [`XmlMapping`](./xmlmapping/) egendom.

`StructuredDocumentTag` kan förekomma i ett dokument på följande platser:

* Blocknivå - Bland stycken och tabeller, som underordnad till en[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) eller en[`Shape`](../../aspose.words.drawing/shape/) nod.
* Radnivå - Bland rader i en tabell, som underordnad till en[`Table`](../../aspose.words.tables/table/) nod.
* Cellnivå - Bland celler i en tabellrad, som underordnad till en[`Row`](../../aspose.words.tables/row/) nod.
* Inline-nivå - Bland inline-innehåll inuti, som underordnad enhet till en[`Paragraph`](../../aspose.words/paragraph/).
* Kapslad inuti en annan`StructuredDocumentTag`.

## Exempel

Visar hur man arbetar med stilar för innehållskontrollelement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två sätt att tillämpa en stil från dokumentet på en strukturerad dokumenttagg.
// 1 - Använd ett stilobjekt från dokumentets stilsamling:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Referera till en stil i dokumentet med namn:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Se även

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
