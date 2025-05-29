---
title: BuildingBlock Class
linktitle: BuildingBlock
articleTitle: BuildingBlock
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.BuildingBlocks.BuildingBlock för att skapa och hantera ordlisteposter som AutoText och AutoCorrect för förbättrad dokumenteffektivitet.
type: docs
weight: 320
url: /sv/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

Representerar en post i ett ordlistadokument, till exempel ett byggblock, en autotext eller en autokorrigeringspost.

För att lära dig mer, besök[Aspose.Words-dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public class BuildingBlock : CompositeNode
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [BuildingBlock](buildingblock/)(*[GlossaryDocument](../glossarydocument/)*) | Initierar en ny instans av den här klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | Anger beteendet som ska tillämpas när innehållet i byggblocket infogas i huvuddokumentet. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | Anger kategoriseringen på andra nivån för byggblocket. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Hämtar antalet omedelbara barn till denna nod. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | Hämtar eller anger beskrivningen som är associerad med detta byggblock. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Hämtar nodens första barn. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | Hämtar den första sektionen i byggblocket. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | Anger den första kategoriseringen för byggblocket i syfte att klassificera eller sortera användargränssnittet. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | Hämtar eller ställer in en identifierare (ett 128-bitars GUID) som unikt identifierar detta byggblock. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returer`sann` om den här noden har några undernoder. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returer`sann` eftersom denna nod kan ha underordnade noder. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Hämtar nodens sista barn. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | Hämtar den sista sektionen i byggblocket. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | Hämtar eller anger namnet på detta byggblock. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | ReturnerarBuildingBlock värde. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | Returnerar en samling som representerar alla sektioner i byggblocket. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | Anger byggstenstypen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Tar emot en besökare. |
| override [AcceptEnd](../../aspose.words.buildingblocks/buildingblock/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka slutet av byggblocket. |
| override [AcceptStart](../../aspose.words.buildingblocks/buildingblock/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare för att besöka början av byggblocket. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Lägger till den angivna noden i slutet av listan över underordnade noder för denna nod. |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tar bort alla[`SmartTag`](../../aspose.words.markup/smarttag/) underordnade noder till den aktuella noden. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Väljer en lista med noder som matchar XPath-uttrycket. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Väljer den första[`Node`](../../aspose.words/node/) som matchar XPath-uttrycket. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

`BuildingBlock` kan endast innehålla[`Section`](../../aspose.words/section/) noder.

`BuildingBlock` kan bara vara ett barn av[`GlossaryDocument`](../glossarydocument/).

Du kan skapa nya byggstenar och infoga dem i ett ordlistadokument. Du kan ändra eller ta bort befintliga byggstenar. Du kan kopiera eller flytta byggstenar mellan dokument. Du kan infoga innehållet i ett byggsten i ett dokument.

Motsvarar den**docPart** ,**docPartPr** och**docPartBody**element i OOXML.

## Exempel

Visar hur man lägger till ett anpassat byggblock i ett dokument.

```csharp
public void CreateAndInsert()
{
    // Ett dokuments ordlista innehåller byggstenar.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Skapa en byggsten, namnge den och lägg sedan till den i ordlistadokumentet.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Alla nya byggblocks-GUID:er har samma nollvärde som standard, och vi kan ge dem ett nytt unikt värde.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Följande egenskaper kategoriserar byggstenar
    // i menyn som vi kan komma åt i Microsoft Word via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Innan vi kan lägga till den här byggstenen i vårt dokument måste vi ge den lite innehåll,
    // vilket vi kommer att göra med hjälp av en dokumentbesökare. Denna besökare kommer också att ange en kategori, ett galleri och ett beteende.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    // Besök början/slut av BuildingBlock.
    block.Accept(visitor);

    // Vi kan komma åt blocket som vi just skapade från ordlistadokumentet.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Själva blocket är en sektion som innehåller texten.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // Nu kan vi infoga det i dokumentet som ett nytt avsnitt.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Vi kan också hitta den i Microsoft Words Building Blocks Organizer och placera den manuellt.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Ställer in ett besökt byggblock som ska infogas i dokumentet som en snabbdel och lägger till text i dess innehåll.
/// </summary>
public class BuildingBlockVisitor : DocumentVisitor
{
    public BuildingBlockVisitor(GlossaryDocument ownerGlossaryDoc)
    {
        mBuilder = new StringBuilder();
        mGlossaryDoc = ownerGlossaryDoc;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        // Konfigurera byggblocket som en snabbdel och lägg till egenskaper som används av Building Blocks Organizer.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Lägg till ett avsnitt med text.
        // Om blocket infogas i dokumentet läggs det här avsnittet till med dess underordnade noder på platsen.
        Section section = new Section(mGlossaryDoc);
        block.AppendChild(section);
        block.FirstSection.EnsureMinimum();

        Run run = new Run(mGlossaryDoc, "Text inside " + block.Name);
        block.FirstSection.Body.FirstParagraph.AppendChild(run);

        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.Append("Visited " + block.Name + "\r\n");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
    private readonly GlossaryDocument mGlossaryDoc;
}
```

### Se även

* class [CompositeNode](../../aspose.words/compositenode/)
* namnutrymme [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* hopsättning [Aspose.Words](../../)
