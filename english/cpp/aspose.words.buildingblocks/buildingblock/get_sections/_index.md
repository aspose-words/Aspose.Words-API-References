---
title: Aspose::Words::BuildingBlocks::BuildingBlock::get_Sections method
linktitle: get_Sections
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::BuildingBlock::get_Sections method. Returns a collection that represents all sections in the building block in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.buildingblocks/buildingblock/get_sections/
---
## BuildingBlock::get_Sections method


Returns a collection that represents all sections in the building block.

```cpp
System::SharedPtr<Aspose::Words::SectionCollection> Aspose::Words::BuildingBlocks::BuildingBlock::get_Sections()
```


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

## See Also

* Class [SectionCollection](../../../aspose.words/sectioncollection/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
