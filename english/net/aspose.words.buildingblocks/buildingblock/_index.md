---
title: BuildingBlock Class
linktitle: BuildingBlock
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.BuildingBlocks.BuildingBlock class. Represents a glossary document entry such as a Building Block AutoText or an AutoCorrect entry in C#.
type: docs
weight: 120
url: /net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

Represents a glossary document entry such as a Building Block, AutoText or an AutoCorrect entry.

To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```csharp
public class BuildingBlock : CompositeNode
```

## Constructors

| Name | Description |
| --- | --- |
| [BuildingBlock](buildingblock/)(*[GlossaryDocument](../glossarydocument/)*) | Initializes a new instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | Specifies the second-level categorization for the building block. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | Gets or sets the description associated with this building block. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | Gets the first section in the building block. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | Gets or sets an identifier (a 128-bit GUID) that uniquely identifies this building block. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns `true` as this node can have child nodes. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | Gets the last section in the building block. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | Gets or sets the name of this building block. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | Returns the BuildingBlock value. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | Returns a collection that represents all sections in the building block. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | Specifies the building block type. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Creates navigator which can be used to traverse and read nodes. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Gets the first ancestor of the specified [`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Provides support for the for each style iteration over the child nodes of this node. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [`SmartTag`](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selects the first [`Node`](../../aspose.words/node/) that matches the XPath expression. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exports the content of the node into a string using the specified save options. |

## Remarks

`BuildingBlock` can contain only [`Section`](../../aspose.words/section/) nodes.

`BuildingBlock` can only be a child of [`GlossaryDocument`](../glossarydocument/).

You can create new building blocks and insert them into a glossary document. You can modify or delete existing building blocks. You can copy or move building blocks between documents. You can insert content of a building block into a document.

Corresponds to the **docPart**, **docPartPr** and **docPartBody** elements in OOXML.

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

* class [CompositeNode](../../aspose.words/compositenode/)
* namespace [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* assembly [Aspose.Words](../../)
