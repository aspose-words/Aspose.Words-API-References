---
title: BuildingBlock.Guid
linktitle: Guid
articleTitle: Guid
second_title: Aspose.Words for .NET
description: Discover BuildingBlock GUID property. Easily manage a unique 128-bit identifier for your building blocks, ensuring seamless organization and identification.
type: docs
weight: 70
url: /net/aspose.words.buildingblocks/buildingblock/guid/
---
## BuildingBlock.Guid property

Gets or sets an identifier (a 128-bit GUID) that uniquely identifies this building block.

```csharp
public Guid Guid { get; set; }
```

## Remarks

Can be used by an application to uniquely reference a building block regardless of different naming due to localization.

Corresponds to the **docPartPr.guid** element in OOXML.

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
    Assert.That(block.Guid.ToString(), Is.EqualTo("00000000-0000-0000-0000-000000000000"));

    block.Guid = Guid.NewGuid();

    // The following properties categorize building blocks
    // in the menu we can access in Microsoft Word via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
    Assert.That(block.Category, Is.EqualTo("(Empty Category)"));
    Assert.That(block.Type, Is.EqualTo(BuildingBlockType.None));
    Assert.That(block.Gallery, Is.EqualTo(BuildingBlockGallery.All));
    Assert.That(block.Behavior, Is.EqualTo(BuildingBlockBehavior.Content));

    // Before we can add this building block to our document, we will need to give it some contents,
    // which we will do using a document visitor. This visitor will also set a category, gallery, and behavior.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    // Visit start/end of the BuildingBlock.
    block.Accept(visitor);

    // We can access the block that we just made from the glossary document.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // The block itself is a section that contains the text.
    Assert.That(customBlock.FirstSection.Body.FirstParagraph.GetText(), Is.EqualTo($"Text inside {customBlock.Name}\f"));
    Assert.That(customBlock.LastSection, Is.EqualTo(customBlock.FirstSection));
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

* class [BuildingBlock](../)
* namespace [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* assembly [Aspose.Words](../../../)
