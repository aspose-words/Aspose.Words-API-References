---
title: BuildingBlockCollection
second_title: Aspose.Words for C++ API Reference
description: A collection of BuildingBlock objects in the document.
type: docs
weight: 14
url: /cpp/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class


A collection of [BuildingBlock](../buildingblock/) objects in the document.

```cpp
class BuildingBlockCollection : public Aspose::Words::NodeCollection
```

## Methods

| Method | Description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds a node to the end of the collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determines whether a node is in the collection. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Gets the number of nodes in the collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [idx_get](./idx_get/)(int32_t) | Retrieves a building block at the given index. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the zero-based index of the specified node. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts a node into the collection at the specified index. |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the node from the collection and from the document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](./toarray/)() | Copies all building blocks from the collection to a new array of building blocks. |
## Remarks


You do not create instances of this class directly. To access a collection of building blocks use the [BuildingBlocks](../glossarydocument/get_buildingblocks/) property.

## Examples



Shows ways of accessing building blocks in a glossary document. 
```cpp
void GlossaryDocument_()
{
    auto doc = MakeObject<Document>();
    auto glossaryDoc = MakeObject<GlossaryDocument>();

    for (int i = 1; i <= 5; ++i)
    {
        auto block = MakeObject<BuildingBlock>(glossaryDoc);
        block->set_Name(String(u"Block ") + System::Convert::ToString(i));
        glossaryDoc->AppendChild(block);
    }
    ASSERT_EQ(5, glossaryDoc->get_BuildingBlocks()->get_Count());

    doc->set_GlossaryDocument(glossaryDoc);

    // There are various ways of accessing building blocks.
    // 1 -  Get the first/last building blocks in the collection:
    ASSERT_EQ(u"Block 1", glossaryDoc->get_FirstBuildingBlock()->get_Name());
    ASSERT_EQ(u"Block 5", glossaryDoc->get_LastBuildingBlock()->get_Name());

    // 2 -  Get a building block by index:
    ASSERT_EQ(u"Block 2", glossaryDoc->get_BuildingBlocks()->idx_get(1)->get_Name());
    ASSERT_EQ(u"Block 3", glossaryDoc->get_BuildingBlocks()->ToArray()->idx_get(2)->get_Name());

    // 3 -  Get the first building block that matches a gallery, name and category:
    ASSERT_EQ(u"Block 4", glossaryDoc->GetBuildingBlock(BuildingBlockGallery::All, u"(Empty Category)", u"Block 4")->get_Name());

    // We will do that using a custom visitor,
    // which will give every BuildingBlock in the GlossaryDocument a unique GUID
    auto visitor = MakeObject<ExBuildingBlocks::GlossaryDocVisitor>();
    glossaryDoc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;

    // In Microsoft Word, we can access the building blocks via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
    doc->Save(ArtifactsDir + u"BuildingBlocks.GlossaryDocument.dotx");
}

class GlossaryDocVisitor : public DocumentVisitor
{
public:
    GlossaryDocVisitor()
    {
        mBlocksByGuid = MakeObject<System::Collections::Generic::Dictionary<System::Guid, SharedPtr<BuildingBlock>>>();
        mBuilder = MakeObject<System::Text::StringBuilder>();
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    SharedPtr<System::Collections::Generic::Dictionary<System::Guid, SharedPtr<BuildingBlock>>> GetDictionary()
    {
        return mBlocksByGuid;
    }

    VisitorAction VisitGlossaryDocumentStart(SharedPtr<GlossaryDocument> glossary) override
    {
        mBuilder->AppendLine(u"Glossary document found!");
        return VisitorAction::Continue;
    }

    VisitorAction VisitGlossaryDocumentEnd(SharedPtr<GlossaryDocument> glossary) override
    {
        mBuilder->AppendLine(u"Reached end of glossary!");
        mBuilder->AppendLine(String(u"BuildingBlocks found: ") + mBlocksByGuid->get_Count());
        return VisitorAction::Continue;
    }

    VisitorAction VisitBuildingBlockStart(SharedPtr<BuildingBlock> block) override
    {
        block->set_Guid(System::Guid::NewGuid());
        mBlocksByGuid->Add(block->get_Guid(), block);
        return VisitorAction::Continue;
    }

    VisitorAction VisitBuildingBlockEnd(SharedPtr<BuildingBlock> block) override
    {
        mBuilder->AppendLine(String(u"\tVisited block \"") + block->get_Name() + u"\"");
        mBuilder->AppendLine(String(u"\t Type: ") + System::ObjectExt::ToString(block->get_Type()));
        mBuilder->AppendLine(String(u"\t Gallery: ") + System::ObjectExt::ToString(block->get_Gallery()));
        mBuilder->AppendLine(String(u"\t Behavior: ") + System::ObjectExt::ToString(block->get_Behavior()));
        mBuilder->AppendLine(String(u"\t Description: ") + block->get_Description());

        return VisitorAction::Continue;
    }

private:
    SharedPtr<System::Collections::Generic::Dictionary<System::Guid, SharedPtr<BuildingBlock>>> mBlocksByGuid;
    SharedPtr<System::Text::StringBuilder> mBuilder;
};
```

## See Also

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words](../../)
