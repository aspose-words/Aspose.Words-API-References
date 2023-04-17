---
title: Aspose::Words::Fields::FieldDde class
linktitle: FieldDde
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldDde class. Implements the DDE field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 32000
url: /cpp/aspose.words.fields/fielddde/
---
## FieldDde class


Implements the DDE field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldDde : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Gets or sets whether to update this field automatically. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | Gets or sets whether to insert the linked object as a bitmap. |
| [get_InsertAsHtml](./get_insertashtml/)() | Gets or sets whether to insert the linked object as HTML format text. |
| [get_InsertAsPicture](./get_insertaspicture/)() | Gets or sets whether to insert the linked object as a picture. |
| [get_InsertAsRtf](./get_insertasrtf/)() | Gets or sets whether to insert the linked object in rich-text format (RTF). |
| [get_InsertAsText](./get_insertastext/)() | Gets or sets whether to insert the linked object in text-only format. |
| [get_InsertAsUnicode](./get_insertasunicode/)() | Gets or sets whether to insert the linked object as Unicode text. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLinked](./get_islinked/)() | Gets or sets whether to reduce the file size by not storing graphics data with the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_ProgId](./get_progid/)() | Gets or sets the application type of the link information. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_SourceFullName](./get_sourcefullname/)() | Gets or sets the name and location of the source file. |
| [get_SourceItem](./get_sourceitem/)() | Gets or sets the portion of the source file that's being linked. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Setter for [Aspose::Words::Fields::FieldDde::get_AutoUpdate](./get_autoupdate/). |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | Setter for [Aspose::Words::Fields::FieldDde::get_InsertAsBitmap](./get_insertasbitmap/). |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | Setter for [Aspose::Words::Fields::FieldDde::get_InsertAsHtml](./get_insertashtml/). |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | Setter for [Aspose::Words::Fields::FieldDde::get_InsertAsPicture](./get_insertaspicture/). |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | Setter for [Aspose::Words::Fields::FieldDde::get_InsertAsRtf](./get_insertasrtf/). |
| [set_InsertAsText](./set_insertastext/)(bool) | Setter for [Aspose::Words::Fields::FieldDde::get_InsertAsText](./get_insertastext/). |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | Setter for [Aspose::Words::Fields::FieldDde::get_InsertAsUnicode](./get_insertasunicode/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLinked](./set_islinked/)(bool) | Setter for [Aspose::Words::Fields::FieldDde::get_IsLinked](./get_islinked/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldDde::get_ProgId](./get_progid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldDde::get_SourceFullName](./get_sourcefullname/). |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldDde::get_SourceItem](./get_sourceitem/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples



Shows how to use various field types to link to other documents in the local file system, and display their contents. 
```cpp
enum class InsertLinkedObjectAs
{
    Text,
    Unicode,
    Html,
    Rtf,
    Picture,
    Bitmap
};

static void InsertFieldLink(SharedPtr<DocumentBuilder> builder, ExField::InsertLinkedObjectAs insertLinkedObjectAs, String progId, String sourceFullName,
                            String sourceItem, bool shouldAutoUpdate)
{
    auto field = System::DynamicCast<FieldLink>(builder->InsertField(FieldType::FieldLink, true));

    switch (insertLinkedObjectAs)
    {
    case ApiExamples::ExField::InsertLinkedObjectAs::Text:
        field->set_InsertAsText(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Unicode:
        field->set_InsertAsUnicode(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Html:
        field->set_InsertAsHtml(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Rtf:
        field->set_InsertAsRtf(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Picture:
        field->set_InsertAsPicture(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Bitmap:
        field->set_InsertAsBitmap(true);
        break;
    }

    field->set_AutoUpdate(shouldAutoUpdate);
    field->set_ProgId(progId);
    field->set_SourceFullName(sourceFullName);
    field->set_SourceItem(sourceItem);

    builder->Writeln(u"\n");
}

static void InsertFieldDde(SharedPtr<DocumentBuilder> builder, ExField::InsertLinkedObjectAs insertLinkedObjectAs, String progId, String sourceFullName,
                           String sourceItem, bool isLinked, bool shouldAutoUpdate)
{
    auto field = System::DynamicCast<FieldDde>(builder->InsertField(FieldType::FieldDDE, true));

    switch (insertLinkedObjectAs)
    {
    case ApiExamples::ExField::InsertLinkedObjectAs::Text:
        field->set_InsertAsText(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Unicode:
        field->set_InsertAsUnicode(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Html:
        field->set_InsertAsHtml(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Rtf:
        field->set_InsertAsRtf(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Picture:
        field->set_InsertAsPicture(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Bitmap:
        field->set_InsertAsBitmap(true);
        break;
    }

    field->set_AutoUpdate(shouldAutoUpdate);
    field->set_ProgId(progId);
    field->set_SourceFullName(sourceFullName);
    field->set_SourceItem(sourceItem);
    field->set_IsLinked(isLinked);

    builder->Writeln(u"\n");
}

static void InsertFieldDdeAuto(SharedPtr<DocumentBuilder> builder, ExField::InsertLinkedObjectAs insertLinkedObjectAs, String progId, String sourceFullName,
                               String sourceItem, bool isLinked)
{
    auto field = System::DynamicCast<FieldDdeAuto>(builder->InsertField(FieldType::FieldDDEAuto, true));

    switch (insertLinkedObjectAs)
    {
    case ApiExamples::ExField::InsertLinkedObjectAs::Text:
        field->set_InsertAsText(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Unicode:
        field->set_InsertAsUnicode(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Html:
        field->set_InsertAsHtml(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Rtf:
        field->set_InsertAsRtf(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Picture:
        field->set_InsertAsPicture(true);
        break;

    case ApiExamples::ExField::InsertLinkedObjectAs::Bitmap:
        field->set_InsertAsBitmap(true);
        break;
    }

    field->set_ProgId(progId);
    field->set_SourceFullName(sourceFullName);
    field->set_SourceItem(sourceItem);
    field->set_IsLinked(isLinked);
}
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
