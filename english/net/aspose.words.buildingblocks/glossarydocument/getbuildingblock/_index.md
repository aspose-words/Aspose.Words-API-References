---
title: GlossaryDocument.GetBuildingBlock
linktitle: GetBuildingBlock
articleTitle: GetBuildingBlock
second_title: Aspose.Words for .NET
description: Discover the GlossaryDocument GetBuildingBlock method to efficiently locate building blocks by gallery category and name. Enhance your document management today!
type: docs
weight: 90
url: /net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

Finds a building block using the specified gallery, category and name.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| Parameter | Type | Description |
| --- | --- | --- |
| gallery | BuildingBlockGallery | The gallery criteria. |
| category | String | The category criteria. Can be `null`, in which case it will not be used for comparison. |
| name | String | The building block name criteria. |

### Return Value

The matching building block or `null` if a match was not found.

## Remarks

This is a convenience method that iterates over all building blocks in this collection and returns the first building block that matches the specified gallery, category and name.

Microsoft Word organizes building blocks into galleries. The galleries are predefined using the [`BuildingBlockGallery`](../../buildingblockgallery/) enum. Within each gallery, building blocks can be organized into one or more categories. The category name is a string. Each building block has a name. A building block name is not guaranteed to be unique.

## Examples

Shows ways of accessing building blocks in a glossary document.

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

    // There are various ways of accessing building blocks.
    // 1 -  Get the first/last building blocks in the collection:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 -  Get a building block by index:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 -  Get the first building block that matches a gallery, name and category:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // We will do that using a custom visitor,
    // which will give every BuildingBlock in the GlossaryDocument a unique GUID
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // Visit start/end of the Glossary document.
    glossaryDoc.Accept(visitor);
    // Visit only start of the Glossary document.
    glossaryDoc.AcceptStart(visitor);
    // Visit only end of the Glossary document.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // In Microsoft Word, we can access the building blocks via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Gives each building block in a visited glossary document a unique GUID.
/// Stores the GUID-building block pairs in a dictionary.
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

### See Also

* class [BuildingBlock](../../buildingblock/)
* enum [BuildingBlockGallery](../../buildingblockgallery/)
* class [GlossaryDocument](../)
* namespace [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* assembly [Aspose.Words](../../../)
