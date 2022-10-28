---
title: FieldAutoNumLgl
second_title: Aspose.Words for C++ API Reference
description: Implements the AUTONUMLGL field.
type: docs
weight: 157
url: /cpp/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class


Implements the AUTONUMLGL field.

```cpp
class FieldAutoNumLgl : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_RemoveTrailingPeriod](./get_removetrailingperiod/)() | Gets or sets whether to display the number without a trailing period. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_SeparatorCharacter](./get_separatorcharacter/)() | Gets or sets the separator character to be used. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_RemoveTrailingPeriod](./set_removetrailingperiod/)(bool) | Setter for [Aspose::Words::Fields::FieldAutoNumLgl::get_RemoveTrailingPeriod](./get_removetrailingperiod/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SeparatorCharacter](./set_separatorcharacter/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldAutoNumLgl::get_SeparatorCharacter](./get_separatorcharacter/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples




Shows how to organize a document using AUTONUMLGL fields. 
```cpp
void FieldAutoNumLgl_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    const String fillerText =
        String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") +
        u"\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // AUTONUMLGL fields display a number that increments at each AUTONUMLGL field within its current heading level.
    // These fields maintain a separate count for each heading level,
    // and each field also displays the AUTONUMLGL field counts for all heading levels below its own.
    // Changing the count for any heading level resets the counts for all levels above that level to 1.
    // This allows us to organize our document in the form of an outline list.
    // This is the first AUTONUMLGL field at a heading level of 1, displaying "1." in the document.
    InsertNumberedClause(builder, u"\tHeading 1", fillerText, StyleIdentifier::Heading1);

    // This is the second AUTONUMLGL field at a heading level of 1, so it will display "2.".
    InsertNumberedClause(builder, u"\tHeading 2", fillerText, StyleIdentifier::Heading1);

    // This is the first AUTONUMLGL field at a heading level of 2,
    // and the AUTONUMLGL count for the heading level below it is "2", so it will display "2.1.".
    InsertNumberedClause(builder, u"\tHeading 3", fillerText, StyleIdentifier::Heading2);

    // This is the first AUTONUMLGL field at a heading level of 3.
    // Working in the same way as the field above, it will display "2.1.1.".
    InsertNumberedClause(builder, u"\tHeading 4", fillerText, StyleIdentifier::Heading3);

    // This field is at a heading level of 2, and its respective AUTONUMLGL count is at 2, so the field will display "2.2.".
    InsertNumberedClause(builder, u"\tHeading 5", fillerText, StyleIdentifier::Heading2);

    // Incrementing the AUTONUMLGL count for a heading level below this one
    // has reset the count for this level so that this field will display "2.2.1.".
    InsertNumberedClause(builder, u"\tHeading 6", fillerText, StyleIdentifier::Heading3);

    auto isAutoNumLegal = [](SharedPtr<Field> f)
    {
        return f->get_Type() == FieldType::FieldAutoNumLegal;
    };

    for (auto field : System::IterateOver<FieldAutoNumLgl>(doc->get_Range()->get_Fields()->LINQ_Where(isAutoNumLegal)))
    {
        // The separator character, which appears in the field result immediately after the number,
        // is a full stop by default. If we leave this property null,
        // our last AUTONUMLGL field will display "2.2.1." in the document.
        ASSERT_TRUE(field->get_SeparatorCharacter() == nullptr);

        // Setting a custom separator character and removing the trailing period
        // will change that field's appearance from "2.2.1." to "2:2:1".
        // We will apply this to all the fields that we have created.
        field->set_SeparatorCharacter(u":");
        field->set_RemoveTrailingPeriod(true);
        ASSERT_EQ(u" AUTONUMLGL  \\s : \\e", field->GetFieldCode());
    }

    doc->Save(ArtifactsDir + u"Field.AUTONUMLGL.docx");
}

static void InsertNumberedClause(SharedPtr<DocumentBuilder> builder, String heading, String contents, StyleIdentifier headingStyle)
{
    builder->InsertField(FieldType::FieldAutoNumLegal, true);
    builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleIdentifier(headingStyle);
    builder->Writeln(heading);

    // This text will belong to the auto num legal field above it.
    // It will collapse when we click the arrow next to the corresponding AUTONUMLGL field in Microsoft Word.
    builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::BodyText);
    builder->Writeln(contents);
}
```

