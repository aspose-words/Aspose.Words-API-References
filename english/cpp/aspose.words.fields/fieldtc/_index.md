---
title: Aspose::Words::Fields::FieldTC class
linktitle: FieldTC
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldTC class. Implements the TC field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 100000
url: /cpp/aspose.words.fields/fieldtc/
---
## FieldTC class


Implements the TC field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldTC : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                public Aspose::Words::Fields::ITocEntry
```

## Methods

| Method | Description |
| --- | --- |
| [FieldTC](./fieldtc/)() |  |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_EntryLevel](./get_entrylevel/)() | Gets or sets the level of the entry. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_OmitPageNumber](./get_omitpagenumber/)() override | Gets or sets whether page number in TOC should be omitted for this field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_Text](./get_text/)() | Gets or sets the text of the entry. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_TypeIdentifier](./get_typeidentifier/)() | Gets or sets a type identifier for this field (which is typically a letter). |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_EntryLevel](./set_entrylevel/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldTC::get_EntryLevel](./get_entrylevel/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_OmitPageNumber](./set_omitpagenumber/)(bool) | Setter for [Aspose::Words::Fields::FieldTC::get_OmitPageNumber](./get_omitpagenumber/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_Text](./set_text/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldTC::get_Text](./get_text/). |
| [set_TypeIdentifier](./set_typeidentifier/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldTC::get_TypeIdentifier](./get_typeidentifier/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to insert a TOC field, and filter which TC fields end up as entries. 
```cpp
void FieldTocEntryIdentifier()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Insert a TOC field, which will compile all TC fields into a table of contents.
    auto fieldToc = System::DynamicCast<FieldToc>(builder->InsertField(FieldType::FieldTOC, true));

    // Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
    fieldToc->set_EntryIdentifier(u"A");
    fieldToc->set_EntryLevelRange(u"1-3");

    ASSERT_EQ(u" TOC  \\f A \\l 1-3", fieldToc->GetFieldCode());

    // These two entries will appear in the table.
    builder->InsertBreak(BreakType::PageBreak);
    InsertTocEntry(builder, u"TC field 1", u"A", u"1");
    InsertTocEntry(builder, u"TC field 2", u"A", u"2");

    ASSERT_EQ(u" TC  \"TC field 1\" \\n \\f A \\l 1", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());

    // This entry will be omitted from the table because it has a different type from "A".
    InsertTocEntry(builder, u"TC field 3", u"B", u"1");

    // This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
    InsertTocEntry(builder, u"TC field 4", u"A", u"5");

    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"Field.TC.docx");
}

void InsertTocEntry(SharedPtr<DocumentBuilder> builder, String text, String typeIdentifier, String entryLevel)
{
    auto fieldTc = System::DynamicCast<FieldTC>(builder->InsertField(FieldType::FieldTOCEntry, true));
    fieldTc->set_OmitPageNumber(true);
    fieldTc->set_Text(text);
    fieldTc->set_TypeIdentifier(typeIdentifier);
    fieldTc->set_EntryLevel(entryLevel);
}
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
