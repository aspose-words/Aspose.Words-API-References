---
title: BuildingBlock.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words för .NET
description: Upptäck BuildingBlocks Accept-metod för att smidigt engagera besökare och förbättra användarupplevelsen. Frigör din webbplats fulla potential idag!
type: docs
weight: 130
url: /sv/net/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock.Accept method

Tar emot en besökare.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| visitor | DocumentVisitor | Besökaren som kommer att besöka noderna. |

### Returvärde

Sant om alla noder besöktes; falskt om[`DocumentVisitor`](../../../aspose.words/documentvisitor/) stoppade operationen innan alla noder besöktes.

## Anmärkningar

Räknar upp denna nod och alla dess underordnade noder. Varje nod anropar en motsvarande metod.[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

För mer information, se designmönstret för besökare.

Samtal[`VisitBuildingBlockStart`](../../../aspose.words/documentvisitor/visitbuildingblockstart/) , anropar sedan [`Accept`](../../../aspose.words/node/accept/) för alla underordnade noder i detta byggblock, anropar sedan [`VisitBuildingBlockEnd`](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Obs! En byggstensnod och dess underordnade noder besöks inte när du kör en Visitor över en[`Document`](../../../aspose.words/document/) Om du vill köra en Visitor över ett byggblock av typen måste du köra besökaren över[`GlossaryDocument`](../../glossarydocument/) eller samtal`Accept` .

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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [BuildingBlock](../)
* namnutrymme [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* hopsättning [Aspose.Words](../../../)
