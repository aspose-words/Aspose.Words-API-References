---
title: GlossaryDocument.GetBuildingBlock
second_title: Aspose.Words för .NET API Referens
description: GlossaryDocument metod. Hittar ett byggblock med det angivna galleriet kategorin och namnet.
type: docs
weight: 70
url: /sv/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

Hittar ett byggblock med det angivna galleriet, kategorin och namnet.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| gallery | BuildingBlockGallery | Gallerikriterierna. |
| category | String | Kategorikriterierna. Kan vara null, i så fall kommer den inte att användas för jämförelse. |
| name | String | Byggstenens namnkriterier. |

### Returvärde

Den matchande byggstenen eller null om en matchning inte hittades.

### Anmärkningar

Detta är en bekvämlighetsmetod som itererar över alla byggblock i den här samlingen och returnerar det första byggblocket som matchar det angivna galleriet, kategorin och namnet.

Microsoft Word organiserar byggstenar i gallerier. Gallerierna är fördefinierade med hjälp av[`BuildingBlockGallery`](../../buildingblockgallery/) enum. Inom varje galleri kan byggstenar organiseras i en eller flera kategorier. Kategorinamnet är en sträng. Varje byggblock har ett namn. Ett building block -namn är inte garanterat unikt.

### Exempel

Visar sätt att komma åt byggstenar i ett ordlistadokument.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 1" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 2" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 3" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 4" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 5" });

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // Det finns olika sätt att komma åt byggstenar.
    // 1 - Få de första/sista byggstenarna i samlingen:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Få en byggsten efter index:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Få den första byggstenen som matchar ett galleri, namn och kategori:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Vi kommer att göra det med en anpassad besökare,
    // som kommer att ge varje byggnadsblock i ordlistadokumentet en unik GUID
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // I Microsoft Word kan vi komma åt byggstenarna via "Infoga" -> "Snabbdelar" -> "Byggstensarrangör".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Ger varje byggsten i ett besökt ordlistadokument en unik GUID.
/// Lagrar GUID-byggblocksparen i en ordbok.
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

* class [BuildingBlock](../../buildingblock/)
* enum [BuildingBlockGallery](../../buildingblockgallery/)
* class [GlossaryDocument](../)
* namnutrymme [Aspose.Words.BuildingBlocks](../../glossarydocument/)
* hopsättning [Aspose.Words](../../../)


