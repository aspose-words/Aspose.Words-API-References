---
title: Aspose::Words::Fields::FieldDde::get_InsertAsUnicode method
linktitle: get_InsertAsUnicode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldDde::get_InsertAsUnicode method. Gets or sets whether to insert the linked object as Unicode text in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.fields/fielddde/get_insertasunicode/
---
## FieldDde::get_InsertAsUnicode method


Gets or sets whether to insert the linked object as Unicode text.

```cpp
bool Aspose::Words::Fields::FieldDde::get_InsertAsUnicode()
```


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

* Class [FieldDde](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
