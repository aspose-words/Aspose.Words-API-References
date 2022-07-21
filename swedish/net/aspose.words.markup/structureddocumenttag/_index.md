---
title: StructuredDocumentTag
second_title: Aspose.Words för .NET API Referens
description: Representerar en strukturerad dokumenttagg SDT eller innehållskontroll i ett dokument.
type: docs
weight: 3820
url: /sv/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Representerar en strukturerad dokumenttagg (SDT eller innehållskontroll) i ett dokument.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag)(DocumentBase, SdtType, MarkupLevel) | Initierar en ny instans av **Strukturerad dokumenttagg** class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance) { get; set; } | Får/ställer in utseendet på en strukturerad dokumenttagg. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory) { get; set; } | Anger kategori av byggblock för detta **SDT** node. Kan inte vara null. |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery) { get; set; } | Anger typ av byggblock för detta **SDT** . Kan inte vara null. |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype) { get; set; } | Anger typen av kalender för detta **SDT** . Standard ärDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked) { get; set; } | Hämtar/ställer in aktuell status för kryssrutan **SDT** . Standardvärdet för den här egenskapen är false. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Hämtar alla omedelbara underordnade noder för denna nod. |
| [Color](../../aspose.words.markup/structureddocumenttag/color) { get; set; } | Hämtar eller ställer in färgen på den strukturerade dokumenttaggen. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont) { get; } | Teckensnittsformatering som kommer att tillämpas på text som skrivs in **SDT** . |
| [Count](../../aspose.words/compositenode/count) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Anger anpassad nodidentifierare. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat) { get; set; } | Sträng som representerar formatet som datum visas i. Kan inte vara null. Datumen för engelska (USA) är "mm/dd/åååå" |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale) { get; set; } | Tillåter att ställa in/hämta språkformatet för datumet som visas i denna **SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat) { get; set; } | Hämtar/ställer in format i vilket datumet för ett datum SDT lagras när **SDT** är bunden till en XML-nod i dokumentets datalager. Standardvärdet ärDateTime |
| virtual [Document](../../aspose.words/node/document) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont) { get; } | Teckensnittsformatering som kommer att tillämpas på det sista tecknet i text som skrivs in **SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Får det första barnet i noden. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate) { get; set; } | Anger fullständigt datum och tid som senast angavs i detta **SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Returnerar sant om denna nod har några underordnade noder. |
| [Id](../../aspose.words.markup/structureddocumenttag/id) { get; } | Anger ett unikt skrivskyddat beständigt numeriskt ID för detta **SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Returnerar sant eftersom denna nod kan ha underordnade noder. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext) { get; set; } | Anger om innehållet i detta **SDT** ska tolkas att innehålla platshållare text (i motsats till vanligt textinnehåll inom SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary) { get; set; } | Anger om detta **SDT** ska tas bort från WordProcessingML-dokumentet när dess contents ändras. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Hämtar nodens sista underordnade. |
| [Level](../../aspose.words.markup/structureddocumenttag/level) { get; } | Får nivån på vilken detta **SDT** förekommer i dokumentträdet. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems) { get; } | Blir[`SdtListItemCollection`](../sdtlistitemcollection) i samband med detta **SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol) { get; set; } | När den är satt till true kommer den här egenskapen att förbjuda en användare att ta bort detta **SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents) { get; set; } | När den är satt till true kommer den här egenskapen att förbjuda en användare att redigera innehållet i denna **SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline) { get; set; } | Anger om detta **SDT** tillåter flera textrader. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype) { get; } | Returnerar **NodeType.StructuredDocumentTag** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder) { get; } | Får[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) som innehåller platshållartext som ska visas när innehållet i denna SDT-körning är tomt, det associerade mappade XML-elementet är tomt som specificerats via[`XmlMapping`](./xmlmapping) element eller[`IsShowingPlaceholderText`](./isshowingplaceholdertext) element är sant. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername) { get; set; } | Hämtar eller sätter Namn på[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock) som innehåller platshållartext. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range) { get; } | Returnerar en **Räckvidd** objekt som representerar den del av ett dokument som finns i denna nod. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype) { get; } | Får typ av detta **Strukturerad dokumenttagg** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style) { get; set; } | Hämtar eller ställer in stilen för den strukturerade dokumenttaggen. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename) { get; set; } | Hämtar eller ställer in namnet på stilen som tillämpas på den strukturerade dokumenttaggen. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag) { get; set; } | Anger en tagg som är associerad med den aktuella SDT-noden. Kan inte vara null. |
| [Title](../../aspose.words.markup/structureddocumenttag/title) { get; set; } | Anger det vänliga namnet som är associerat med detta **SDT** . Kan inte vara null. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml) { get; } | Får en sträng som representerar XML som finns i noden iFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping) { get; } | Hämtar ett objekt som representerar mappningen av denna strukturerade dokumenttagg till XML data i en anpassad XML-del av det aktuella dokumentet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept)(DocumentVisitor) | Accepterar en besökare. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear)() | Rensar innehållet i denna strukturerade dokumenttagg och visar en platshållare om den är definierad. |
| [Clone](../../aspose.words/node/clone)(bool) | Skapar en dubblett av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserverad för systemanvändning. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Returnerar en aktiv samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Hämtar texten för denna nod och alla dess underordnade. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Returnerar indexet för den angivna undernoden i den underordnade nodmatrisen. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Tar bort alla undernoder för den aktuella noden. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Tar bort den angivna underordnade noden. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly)() | Tar bara bort denna SDT-nod själv, men behåller innehållet i den i dokumentträdet. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Tar bort alla[`SmartTag`](../smarttag) underliggande noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Väljer den första noden som matchar XPath-uttrycket. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol)(int, string) | Ställer in symbolen som används för att representera det kontrollerade tillståndet för en innehållskontroll i kryssrutan. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol)(int, string) | Ställer in symbolen som används för att representera det omarkerade tillståndet för en innehållskontroll i kryssrutan. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

Strukturerade dokumenttaggar (SDT) gör det möjligt att bädda in kunddefinierad semantik såväl som dess beteende och utseende i ett dokument.

denna version tillhandahåller Aspose.Words ett antal offentliga metoder och egenskaper för att manipulera beteendet och innehållet i[`StructuredDocumentTag`](../structureddocumenttag) . Mappning av SDT-noder till anpassade XML-paket i ett dokument kan utföras med hjälp av [`XmlMapping`](./xmlmapping) fast egendom.

[`StructuredDocumentTag`](../structureddocumenttag) kan förekomma i ett dokument på följande platser:

* Blocknivå - Bland stycken och tabeller, som barn till en[`Body`](../../aspose.words/body) ,[`HeaderFooter`](../../aspose.words/headerfooter) , [`Comment`](../../aspose.words/comment) ,[`Footnote`](../../aspose.words.notes/footnote) eller a[`Shape`](../../aspose.words.drawing/shape) nod.
* Radnivå - Bland rader i en tabell, som barn till en[`Table`](../../aspose.words.tables/table) nod.
* Cell-nivå - Bland celler i en tabellrad, som ett barn till en[`Row`](../../aspose.words.tables/row) nod.
* Inline-level - Bland inline-innehåll inuti, som barn till en[`Paragraph`](../../aspose.words/paragraph).
* Kapslad inuti en annan[`StructuredDocumentTag`](../structureddocumenttag).

### Exempel

Visar hur man arbetar med stilar för innehållskontrollelement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns två sätt att tillämpa en stil från dokumentet på en strukturerad dokumenttagg.
// 1 - Använd ett stilobjekt från dokumentets stilsamling:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Referera till en stil i dokumentet efter namn:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Se även

* class [CompositeNode](../../aspose.words/compositenode)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
