---
title: Aspose::Words::BuildingBlocks::BuildingBlockGallery enum
linktitle: BuildingBlockGallery
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::BuildingBlockGallery enum. Specifies the predefined gallery into which a building block is classified in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.buildingblocks/buildingblockgallery/
---
## BuildingBlockGallery enum


Specifies the predefined gallery into which a building block is classified.

```cpp
enum class BuildingBlockGallery
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| All | 0 | Specifies that this glossary document entry shall be associated with all possible gallery classification values. |
| AutoText | 1 |  |
| Bibliography | 2 |  |
| CoverPage | 3 |  |
| CustomAutoText | 4 |  |
| CustomBibliography | 5 |  |
| CustomCoverPage | 6 |  |
| CustomEquations | 7 |  |
| CustomFooters | 8 |  |
| CustomHeaders | 9 |  |
| Custom1 | 10 |  |
| Custom2 | 11 |  |
| Custom3 | 12 |  |
| Custom4 | 13 |  |
| Custom5 | 14 |  |
| CustomPageNumber | 15 |  |
| CustomPageNumberAtBottom | 16 |  |
| CustomPageNumberAtMargin | 17 |  |
| CustomPageNumberAtTop | 18 |  |
| CustomQuickParts | 19 |  |
| CustomTableOfContents | 20 |  |
| CustomTables | 21 |  |
| CustomTextBox | 22 |  |
| CustomWatermarks | 23 |  |
| NoGallery | 24 |  |
| QuickParts | 25 |  |
| Equations | 26 |  |
| Footers | 27 |  |
| Headers | 28 |  |
| PageNumber | 29 |  |
| PageNumberAtBottom | 30 |  |
| PageNumberAtMargin | 31 |  |
| PageNumberAtTop | 32 |  |
| StructuredDocumentTagPlaceholderText | 33 |  |
| TableOfContents | 34 |  |
| Tables | 35 |  |
| TextBox | 36 |  |
| Watermarks | 37 |  |
| Default | n/a | Same as [All](./). |

## Remarks


Corresponds to the **ST_DocPartGallery** type in OOXML.

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

* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
