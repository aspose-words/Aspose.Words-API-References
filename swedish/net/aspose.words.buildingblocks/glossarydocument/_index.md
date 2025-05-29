---
title: GlossaryDocument Class
linktitle: GlossaryDocument
articleTitle: GlossaryDocument
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.BuildingBlocks.GlossaryDocument, din nyckel till att hantera AutoText och Building Blocks sömlöst i Word-dokument.
type: docs
weight: 370
url: /sv/net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

Representerar rotelementet för ett ordlistadokument i ett Word-dokument. Ett ordlistadokument är en lagringsplats för AutoText, Autokorrigeringsposter och byggstenar.

För att lära dig mer, besök[Aspose.Words-dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public class GlossaryDocument : DocumentBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [GlossaryDocument](glossarydocument/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Hämtar eller ställer in dokumentets bakgrundsform. Kan vara`null` . |
| [BuildingBlocks](../../aspose.words.buildingblocks/glossarydocument/buildingblocks/) { get; } | Returnerar en typad samling som representerar alla byggstenar i ordlistadokumentet. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Hämtar denna instans. |
| [FirstBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/firstbuildingblock/) { get; } | Hämtar den första byggstenen i ordlistadokumentet. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Ger åtkomst till egenskaper för teckensnitt som används i detta dokument. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Ger åtkomst till fotnots-/slutnotsavgränsare som definierats i dokumentet. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [LastBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/lastbuildingblock/) { get; } | Hämtar den sista byggstenen i ordlistadokumentet. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Ger åtkomst till listformateringen som används i dokumentet. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Anropas när en nod infogas eller tas bort i dokumentet. |
| override [NodeType](../../aspose.words.buildingblocks/glossarydocument/nodetype/) { get; } | ReturnerarGlossaryDocument värde. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Hämtar eller ställer in dokumentets sidfärg. Den här egenskapen är en enklare version av[`BackgroundShape`](../../aspose.words/documentbase/backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Gör det möjligt att styra hur externa resurser laddas. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Returnerar en samling stilar definierade i dokumentet. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Anropas under olika dokumentbehandlingsprocedurer när ett problem upptäcks som kan resultera i förlust av data- eller formateringsåtergivning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/glossarydocument/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words.buildingblocks/glossarydocument/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka slutet av ordlistadokumentet. |
| override [AcceptStart](../../aspose.words.buildingblocks/glossarydocument/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka början av ordlistadokumentet. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Skapar en navigator som kan användas för att korsa och läsa noder. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/getbuildingblock/)(*[BuildingBlockGallery](../buildingblockgallery/), string, string*) | Hittar ett byggblock med hjälp av det angivna galleriet, kategorin och namnet. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Returnerar en N:te underordnad nod som matchar den angivna typen. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar den angivna typen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool*) | Importerar en nod från ett annat dokument till det aktuella dokumentet. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool, [ImportFormatMode](../../aspose.words/importformatmode/)*) | Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formateringen. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Returnerar indexet för den angivna undernoden i undernodsmatrisen. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Infogar den angivna noden omedelbart efter den angivna referensnoden. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Infogar den angivna noden omedelbart före den angivna referensnoden. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Lägger till den angivna noden i början av listan över underordnade noder för denna nod. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Tar bort alla undernoder till den aktuella noden. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Tar bort den angivna undernoden. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underordnade noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../../aspose.words/node/) som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

Vissa dokument, vanligtvis mallar, kan innehålla Autotext, Autokorrigering poster och/eller byggstenar (även kalladeordlista dokumentposter ,dokumentdelar ellerbyggstenar).

För att komma åt byggstenar måste du ladda ett dokument i en[`Document`](../../aspose.words/document/) -objektet. Byggstenar kommer att finnas tillgängliga via[`GlossaryDocument`](../../aspose.words/document/glossarydocument/) egendom.

`GlossaryDocument` kan innehålla valfritt antal[`BuildingBlock`](../buildingblock/)objekt. Varje[`BuildingBlock`](../buildingblock/) representerar en del av dokumentet.

Motsvarar den**ordlistaDokument** och**docParts**element i OOXML.

## Exempel

Visar sätt att komma åt byggstenar i ett ordlistadokument.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    BuildingBlock child1 = new BuildingBlock(glossaryDoc) { Name = "Block 1" };
    glossaryDoc.AppendChild(child1);
    BuildingBlock child2 = new BuildingBlock(glossaryDoc) { Name = "Block 2" };
    glossaryDoc.AppendChild(child2);
    BuildingBlock child3 = new BuildingBlock(glossaryDoc) { Name = "Block 3" };
    glossaryDoc.AppendChild(child3);
    BuildingBlock child4 = new BuildingBlock(glossaryDoc) { Name = "Block 4" };
    glossaryDoc.AppendChild(child4);
    BuildingBlock child5 = new BuildingBlock(glossaryDoc) { Name = "Block 5" };
    glossaryDoc.AppendChild(child5);

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // Det finns olika sätt att komma åt byggstenar.
    // 1 - Hämta de första/sista byggstenarna i samlingen:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Hämta en byggsten via index:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Hämta den första byggstenen som matchar ett galleri, namn och kategori:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Vi gör det med hjälp av en anpassad besökare,
    // vilket ger varje BuildingBlock i GlossaryDocument ett unikt GUID
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // Besök början/slutet av ordlistadokumentet.
    glossaryDoc.Accept(visitor);
    // Besök endast början av ordlistadokumentet.
    glossaryDoc.AcceptStart(visitor);
    // Besök endast slutet av ordlistadokumentet.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // I Microsoft Word kan vi komma åt byggstenarna via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Ger varje byggsten i ett besökt ordlistadokument ett unikt GUID.
/// Lagrar GUID-byggstensparen i en ordbok.
/// </summary>
public class GlossaryDocVisitor : DocumentVisitor
{
    public GlossaryDocVisitor()
    {
        mBlocksByGuid = new Dictionary<Guid, BuildingBlock>();
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public Dictionary<Guid, BuildingBlock> GetDictionary()
    {
        return mBlocksByGuid;
    }

    public override VisitorAction VisitGlossaryDocumentStart(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Glossary document found!");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGlossaryDocumentEnd(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Reached end of glossary!");
        mBuilder.AppendLine("BuildingBlocks found: " + mBlocksByGuid.Count);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        block.Guid = Guid.NewGuid();
        mBlocksByGuid.Add(block.Guid, block);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.AppendLine("\tVisited block \"" + block.Name + "\"");
        mBuilder.AppendLine("\t Type: " + block.Type);
        mBuilder.AppendLine("\t Gallery: " + block.Gallery);
        mBuilder.AppendLine("\t Behavior: " + block.Behavior);
        mBuilder.AppendLine("\t Description: " + block.Description);

        return VisitorAction.Continue;
    }

    private readonly Dictionary<Guid, BuildingBlock> mBlocksByGuid;
    private readonly StringBuilder mBuilder;
}
```

### Se även

* class [DocumentBase](../../aspose.words/documentbase/)
* namnutrymme [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* hopsättning [Aspose.Words](../../)
