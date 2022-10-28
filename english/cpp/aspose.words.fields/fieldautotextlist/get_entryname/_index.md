---
title: get_EntryName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the AutoText entry.
type: docs
weight: 1
url: /cpp/aspose.words.fields/fieldautotextlist/get_entryname/
---
## FieldAutoTextList.get_EntryName method


Gets or sets the name of the AutoText entry.

```cpp
System::String Aspose::Words::Fields::FieldAutoTextList::get_EntryName()
```


## Examples




Shows how to use an AUTOTEXTLIST field to select from a list of AutoText entries. 
```cpp
void FieldAutoTextList_()
{
    auto doc = MakeObject<Document>();

    // Create a glossary document and populate it with auto text entries.
    doc->set_GlossaryDocument(MakeObject<GlossaryDocument>());
    AppendAutoTextEntry(doc->get_GlossaryDocument(), u"AutoText 1", u"Contents of AutoText 1");
    AppendAutoTextEntry(doc->get_GlossaryDocument(), u"AutoText 2", u"Contents of AutoText 2");
    AppendAutoTextEntry(doc->get_GlossaryDocument(), u"AutoText 3", u"Contents of AutoText 3");

    auto builder = MakeObject<DocumentBuilder>(doc);

    // Create an AUTOTEXTLIST field and set the text that the field will display in Microsoft Word.
    // Set the text to prompt the user to right-click this field to select an AutoText building block,
    // whose contents the field will display.
    auto field = System::DynamicCast<FieldAutoTextList>(builder->InsertField(FieldType::FieldAutoTextList, true));
    field->set_EntryName(u"Right click here to select an AutoText block");
    field->set_ListStyle(u"Heading 1");
    field->set_ScreenTip(u"Hover tip text for AutoTextList goes here");

    ASSERT_EQ(String(u" AUTOTEXTLIST  \"Right click here to select an AutoText block\" ") + u"\\s \"Heading 1\" " +
                  u"\\t \"Hover tip text for AutoTextList goes here\"",
              field->GetFieldCode());

    doc->Save(ArtifactsDir + u"Field.AUTOTEXTLIST.dotx");
}

static void AppendAutoTextEntry(SharedPtr<GlossaryDocument> glossaryDoc, String name, String contents)
{
    auto buildingBlock = MakeObject<BuildingBlock>(glossaryDoc);
    buildingBlock->set_Name(name);
    buildingBlock->set_Gallery(BuildingBlockGallery::AutoText);
    buildingBlock->set_Category(u"General");
    buildingBlock->set_Behavior(BuildingBlockBehavior::Paragraph);

    auto section = MakeObject<Section>(glossaryDoc);
    section->AppendChild(MakeObject<Body>(glossaryDoc));
    section->get_Body()->AppendParagraph(contents);
    buildingBlock->AppendChild(section);

    glossaryDoc->AppendChild(buildingBlock);
}
```

