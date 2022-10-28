---
title: FieldAutoTextList
second_title: Aspose.Words for C++ API Reference
description: Implements the AUTOTEXTLIST field.
type: docs
weight: 196
url: /cpp/aspose.words.fields/fieldautotextlist/
---
## FieldAutoTextList class


Implements the AUTOTEXTLIST field.

```cpp
class FieldAutoTextList : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_EntryName](./get_entryname/)() | Gets or sets the name of the AutoText entry. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_ListStyle](./get_liststyle/)() | Gets or sets the name of the style on which the list to contain entries is based. |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_ScreenTip](./get_screentip/)() | Gets or sets the text of the ScreenTip to show. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_EntryName](./set_entryname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldAutoTextList::get_EntryName](./get_entryname/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_ListStyle](./set_liststyle/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldAutoTextList::get_ListStyle](./get_liststyle/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldAutoTextList::get_ScreenTip](./get_screentip/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

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

