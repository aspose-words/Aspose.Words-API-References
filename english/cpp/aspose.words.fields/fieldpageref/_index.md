---
title: FieldPageRef
second_title: Aspose.Words for C++ API Reference
description: Implements the PAGEREF field.
type: docs
weight: 1015
url: /cpp/aspose.words.fields/fieldpageref/
---
## FieldPageRef class


Implements the PAGEREF field.

```cpp
class FieldPageRef : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Gets or sets the name of the bookmark. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Gets or sets whether to insert a hyperlink to the bookmarked paragraph. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Gets or sets whether to insert a relative position of the bookmarked paragraph. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldPageRef::get_BookmarkName](./get_bookmarkname/). |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Setter for [Aspose::Words::Fields::FieldPageRef::get_InsertHyperlink](./get_inserthyperlink/). |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Setter for [Aspose::Words::Fields::FieldPageRef::get_InsertRelativePosition](./get_insertrelativeposition/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows to insert PAGEREF fields to display the relative location of bookmarks. 
```cpp
void FieldPageRef_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    InsertAndNameBookmark(builder, u"MyBookmark1");

    // Insert a PAGEREF field that displays what page a bookmark is on.
    // Set the InsertHyperlink flag to make the field also function as a clickable link to the bookmark.
    ASSERT_EQ(u" PAGEREF  MyBookmark3 \\h", InsertFieldPageRef(builder, u"MyBookmark3", true, false, u"Hyperlink to Bookmark3, on page: ")->GetFieldCode());

    // We can use the \p flag to get the PAGEREF field to display
    // the bookmark's position relative to the position of the field.
    // Bookmark1 is on the same page and above this field, so this field's displayed result will be "above".
    ASSERT_EQ(u" PAGEREF  MyBookmark1 \\h \\p", InsertFieldPageRef(builder, u"MyBookmark1", true, true, u"Bookmark1 is ")->GetFieldCode());

    // Bookmark2 will be on the same page and below this field, so this field's displayed result will be "below".
    ASSERT_EQ(u" PAGEREF  MyBookmark2 \\h \\p", InsertFieldPageRef(builder, u"MyBookmark2", true, true, u"Bookmark2 is ")->GetFieldCode());

    // Bookmark3 will be on a different page, so the field will display "on page 2".
    ASSERT_EQ(u" PAGEREF  MyBookmark3 \\h \\p", InsertFieldPageRef(builder, u"MyBookmark3", true, true, u"Bookmark3 is ")->GetFieldCode());

    InsertAndNameBookmark(builder, u"MyBookmark2");
    builder->InsertBreak(BreakType::PageBreak);
    InsertAndNameBookmark(builder, u"MyBookmark3");

    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"Field.PAGEREF.docx");
}

static SharedPtr<FieldPageRef> InsertFieldPageRef(SharedPtr<DocumentBuilder> builder, String bookmarkName, bool insertHyperlink,
                                                  bool insertRelativePosition, String textBefore)
{
    builder->Write(textBefore);

    auto field = System::DynamicCast<FieldPageRef>(builder->InsertField(FieldType::FieldPageRef, true));
    field->set_BookmarkName(bookmarkName);
    field->set_InsertHyperlink(insertHyperlink);
    field->set_InsertRelativePosition(insertRelativePosition);
    builder->Writeln();

    return field;
}

static void InsertAndNameBookmark(SharedPtr<DocumentBuilder> builder, String bookmarkName)
{
    builder->StartBookmark(bookmarkName);
    builder->Writeln(String::Format(u"Contents of bookmark \"{0}\".", bookmarkName));
    builder->EndBookmark(bookmarkName);
}
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words](../../)
