---
title: Accept
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 130
url: /net/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock.Accept method

Accepts a visitor.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | DocumentVisitor | The visitor that will visit the nodes. |

### Return Value

True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes.

## Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.

Calls [`VisitBuildingBlockStart`](../../../aspose.words/documentvisitor/visitbuildingblockstart), then calls [`Accept`](../../../aspose.words/node/accept) for all child nodes of this building block, then calls [`VisitBuildingBlockEnd`](../../../aspose.words/documentvisitor/visitbuildingblockend).

Note: A building block node and its children are not visited when you execute a Visitor over a [`Document`](../../../aspose.words/document). If you want to execute a Visitor over a building block, you need to execute the visitor over [`GlossaryDocument`](../../glossarydocument) or call `Accept`.

## Examples

Shows how to add a custom building block to a document.

```csharp
public void CreateAndInsert()
{
    // A document's glossary document stores building blocks.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Create a building block, name it, and then add it to the glossary document.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // All new building block GUIDs have the same zero value by default, and we can give them a new unique value.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // The following properties categorize building blocks
    // in the menu we can access in Microsoft Word via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Before we can add this building block to our document, we will need to give it some contents,
    // which we will do using a document visitor. This visitor will also set a category, gallery, and behavior.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // We can access the block that we just made from the glossary document.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // The block itself is a section that contains the text.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);

    // Now, we can insert it into the document as a new section.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // We can also find it in Microsoft Word's Building Blocks Organizer and place it manually.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Sets up a visited building block to be inserted into the document as a quick part and adds text to its contents.
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
        // Configure the building block as a quick part, and add properties used by Building Blocks Organizer.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Add a section with text.
        // Inserting the block into the document will append this section with its child nodes at the location.
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

### See Also

* class [DocumentVisitor](../../../aspose.words/documentvisitor)
* class [BuildingBlock](../../buildingblock)
* namespace [Aspose.Words.BuildingBlocks](../../buildingblock)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
