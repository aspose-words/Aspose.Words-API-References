---
title: Aspose::Words::Fields::FieldAutoNumLgl::get_RemoveTrailingPeriod method
linktitle: get_RemoveTrailingPeriod
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldAutoNumLgl::get_RemoveTrailingPeriod method. Gets or sets whether to display the number without a trailing period in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldautonumlgl/get_removetrailingperiod/
---
## FieldAutoNumLgl::get_RemoveTrailingPeriod method


Gets or sets whether to display the number without a trailing period.

```cpp
bool Aspose::Words::Fields::FieldAutoNumLgl::get_RemoveTrailingPeriod()
```


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

## See Also

* Class [FieldAutoNumLgl](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
