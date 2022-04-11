---
title: GlossaryDocument
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 170
url: /net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

Represents the root element for a glossary document within a Word document. A glossary document is a storage for AutoText, AutoCorrect entries and Building Blocks.

```csharp
public class GlossaryDocument : DocumentBase
```

## Public Members

| Name | Description |
| --- | --- |
| [GlossaryDocument](glossarydocument)() | The default constructor. |
| [BuildingBlocks](buildingblocks) { get; } | Returns a typed collection that represents all building blocks in the glossary document. |
| [FirstBuildingBlock](firstbuildingblock) { get; } | Gets the first building block in the glossary document. |
| [LastBuildingBlock](lastbuildingblock) { get; } | Gets the last building block in the glossary document. |
| override [NodeType](nodetype) { get; } | Returns the GlossaryDocument value. |
| override [Accept](accept)(…) | Accepts a visitor. |
| [GetBuildingBlock](getbuildingblock)(…) | Finds a building block using the specified gallery, category and name. |

### Remarks

Some documents, usually templates, can contain AutoText, AutoCorrect entries and/or Building Blocks (also known as glossary document entries, document parts or building blocks).

To access building blocks, you need to load a document into a [`Document`](../../aspose.words/document) object. Building blocks will be available via the [`GlossaryDocument`](../../aspose.words/document/glossarydocument) property.

[`GlossaryDocument`](../glossarydocument) can contain any number of [`BuildingBlock`](../buildingblock) objects. Each [`BuildingBlock`](../buildingblock) represents one document part.

Corresponds to the glossaryDocument and docParts elements in OOXML.

### Examples

Shows ways of accessing building blocks in a glossary document.

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
    glossaryDoc.Accept(visitor);

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

* class [DocumentBase](../../aspose.words/documentbase)
* namespace [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
