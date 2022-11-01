---
title: BuildingBlock
second_title: Aspose.Words for C++ API Reference
description: Represents a glossary document entry such as a Building Block, AutoText or an AutoCorrect entry.
type: docs
weight: 1
url: /cpp/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class


Represents a glossary document entry such as a Building Block, AutoText or an AutoCorrect entry.

```cpp
class BuildingBlock : public Aspose::Words::CompositeNode
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the end of the list of child nodes for this node. |
| [BuildingBlock](./buildingblock/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Initializes a new instance of this class. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [get_Behavior](./get_behavior/)() const | Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document. |
| [get_Category](./get_category/)() const | Specifies the second-level categorization for the building block. |
| [get_ChildNodes](../../aspose.words/compositenode/get_childnodes/)() | Gets all immediate child nodes of this node. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| [get_Description](./get_description/)() const | Gets or sets the description associated with this building block. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_FirstSection](./get_firstsection/)() | Gets the first section in the building block. |
| [get_Gallery](./get_gallery/)() const | Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting. |
| [get_Guid](./get_guid/)() const | Gets or sets an identifier (a 128-bit GUID) that uniquely identifies this building block. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns true if this node has any child nodes. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns true as this node can have child nodes. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_LastSection](./get_lastsection/)() | Gets the last section in the building block. |
| [get_Name](./get_name/)() const | Gets or sets the name of this building block. |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns the **BuildingBlock** value. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [get_Sections](./get_sections/)() | Returns a collection that represents all sections in the building block. |
| [get_Type](./get_type/)() const | Specifies the building block type. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| [set_Behavior](./set_behavior/)(Aspose::Words::BuildingBlocks::BuildingBlockBehavior) | Setter for [Aspose::Words::BuildingBlocks::BuildingBlock::get_Behavior](./get_behavior/). |
| [set_Category](./set_category/)(const System::String\&) | Setter for [Aspose::Words::BuildingBlocks::BuildingBlock::get_Category](./get_category/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Description](./set_description/)(const System::String\&) | Setter for [Aspose::Words::BuildingBlocks::BuildingBlock::get_Description](./get_description/). |
| [set_Gallery](./set_gallery/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery) | Setter for [Aspose::Words::BuildingBlocks::BuildingBlock::get_Gallery](./get_gallery/). |
| [set_Guid](./set_guid/)(System::Guid) | Setter for [Aspose::Words::BuildingBlocks::BuildingBlock::get_Guid](./get_guid/). |
| [set_Name](./set_name/)(const System::String\&) | Setter for [Aspose::Words::BuildingBlocks::BuildingBlock::get_Name](./get_name/). |
| [set_Type](./set_type/)(Aspose::Words::BuildingBlocks::BuildingBlockType) | Setter for [Aspose::Words::BuildingBlocks::BuildingBlock::get_Type](./get_type/). |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |

[BuildingBlock](./) can contain only [Section](../../aspose.words/section/) nodes.

[BuildingBlock](./) can only be a child of [GlossaryDocument](../glossarydocument/).

You can create new building blocks and insert them into a glossary document. You can modify or delete existing building blocks. You can copy or move building blocks between documents. You can insert content of a building block into a document.

Corresponds to the **docPart**, **docPartPr** and **docPartBody** elements in OOXML.

## Examples




Shows how to add a custom building block to a document. 
```cpp
void CreateAndInsert()
{
    // A document's glossary document stores building blocks.
    auto doc = MakeObject<Document>();
    auto glossaryDoc = MakeObject<GlossaryDocument>();
    doc->set_GlossaryDocument(glossaryDoc);

    // Create a building block, name it, and then add it to the glossary document.
    auto block = MakeObject<BuildingBlock>(glossaryDoc);
    block->set_Name(u"Custom Block");

    glossaryDoc->AppendChild(block);

    // All new building block GUIDs have the same zero value by default, and we can give them a new unique value.
    ASSERT_EQ(u"00000000-0000-0000-0000-000000000000", System::ObjectExt::ToString(block->get_Guid()));

    block->set_Guid(System::Guid::NewGuid());

    // The following properties categorize building blocks
    // in the menu we can access in Microsoft Word via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
    ASSERT_EQ(u"(Empty Category)", block->get_Category());
    ASSERT_EQ(BuildingBlockType::None, block->get_Type());
    ASSERT_EQ(BuildingBlockGallery::All, block->get_Gallery());
    ASSERT_EQ(BuildingBlockBehavior::Content, block->get_Behavior());

    // Before we can add this building block to our document, we will need to give it some contents,
    // which we will do using a document visitor. This visitor will also set a category, gallery, and behavior.
    auto visitor = MakeObject<ExBuildingBlocks::BuildingBlockVisitor>(glossaryDoc);
    block->Accept(visitor);

    // We can access the block that we just made from the glossary document.
    SharedPtr<BuildingBlock> customBlock = glossaryDoc->GetBuildingBlock(BuildingBlockGallery::QuickParts, u"My custom building blocks", u"Custom Block");

    // The block itself is a section that contains the text.
    ASSERT_EQ(String::Format(u"Text inside {0}\f", customBlock->get_Name()), customBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText());
    ASPOSE_ASSERT_EQ(customBlock->get_FirstSection(), customBlock->get_LastSection());
    std::function<void()> parseGuid = [&customBlock]()
    {
        System::Guid::Parse(System::ObjectExt::ToString(customBlock->get_Guid()));
    };

    // Now, we can insert it into the document as a new section.
    doc->AppendChild(doc->ImportNode(customBlock->get_FirstSection(), true));

    // We can also find it in Microsoft Word's Building Blocks Organizer and place it manually.
    doc->Save(ArtifactsDir + u"BuildingBlocks.CreateAndInsert.dotx");
}

class BuildingBlockVisitor : public DocumentVisitor
{
public:
    BuildingBlockVisitor(SharedPtr<GlossaryDocument> ownerGlossaryDoc)
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
        mGlossaryDoc = ownerGlossaryDoc;
    }

    VisitorAction VisitBuildingBlockStart(SharedPtr<BuildingBlock> block) override
    {
        // Configure the building block as a quick part, and add properties used by Building Blocks Organizer.
        block->set_Behavior(BuildingBlockBehavior::Paragraph);
        block->set_Category(u"My custom building blocks");
        block->set_Description(u"Using this block in the Quick Parts section of word will place its contents at the cursor.");
        block->set_Gallery(BuildingBlockGallery::QuickParts);

        // Add a section with text.
        // Inserting the block into the document will append this section with its child nodes at the location.
        auto section = MakeObject<Section>(mGlossaryDoc);
        block->AppendChild(section);
        block->get_FirstSection()->EnsureMinimum();

        auto run = MakeObject<Run>(mGlossaryDoc, String(u"Text inside ") + block->get_Name());
        block->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(run);

        return VisitorAction::Continue;
    }

    VisitorAction VisitBuildingBlockEnd(SharedPtr<BuildingBlock> block) override
    {
        mBuilder->Append(String(u"Visited ") + block->get_Name() + u"\r\n");
        return VisitorAction::Continue;
    }

private:
    SharedPtr<System::Text::StringBuilder> mBuilder;
    SharedPtr<GlossaryDocument> mGlossaryDoc;
};
```

