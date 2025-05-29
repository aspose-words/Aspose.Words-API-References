---
title: Document.GlossaryDocument
linktitle: GlossaryDocument
articleTitle: GlossaryDocument
second_title: Aspose.Words för .NET
description: Upptäck hur du hanterar din dokumentordlista effektivt. Lär dig att skapa och hämta ordlisteposter för AutoText och Building Blocks i dina mallar.
type: docs
weight: 180
url: /sv/net/aspose.words/document/glossarydocument/
---
## Document.GlossaryDocument property

Hämtar eller ställer in ordlistadokumentet i detta dokument eller denna mall. Ett ordlistadokument är ett lagringsutrymme för AutoText-, Autokorrigerings- och Byggblocksposter som definierats i ett dokument.

```csharp
public GlossaryDocument GlossaryDocument { get; set; }
```

## Anmärkningar

Den här egenskapen returnerar`null` om dokumentet inte har ett ordlistadokument.

Du kan lägga till ett ordlistadokument i ett dokument genom att skapa a [`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument/) objekt och tilldela till den här egenskapen.

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

* class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
