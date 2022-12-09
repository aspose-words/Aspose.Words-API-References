---
title: get_InsertAsText
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether to insert the linked object in text-only format.
type: docs
weight: 79
url: /cpp/aspose.words.fields/fielddde/get_insertastext/
---
## FieldDde::get_InsertAsText method


Gets or sets whether to insert the linked object in text-only format.

```cpp
bool Aspose::Words::Fields::FieldDde::get_InsertAsText()
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
void FieldLinkedObjectsAsText(ExField::InsertLinkedObjectAs insertLinkedObjectAs)
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Below are three types of fields we can use to display contents from a linked document in the form of text.
    // 1 -  A LINK field:
    builder->Writeln(u"FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, u"Word.Document.8", MyDir + u"Document.docx", nullptr, true);

    // 2 -  A DDE field:
    builder->Writeln(u"FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, u"Excel.Sheet", MyDir + u"Spreadsheet.xlsx", u"Sheet1!R1C1", true, true);

    // 3 -  A DDEAUTO field:
    builder->Writeln(u"FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, u"Excel.Sheet", MyDir + u"Spreadsheet.xlsx", u"Sheet1!R1C1", true);

    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"Field.LINK.DDE.DDEAUTO.docx");
}

void FieldLinkedObjectsAsImage(ExField::InsertLinkedObjectAs insertLinkedObjectAs)
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Below are three types of fields we can use to display contents from a linked document in the form of an image.
    // 1 -  A LINK field:
    builder->Writeln(u"FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, u"Excel.Sheet", MyDir + u"MySpreadsheet.xlsx", u"Sheet1!R2C2", true);

    // 2 -  A DDE field:
    builder->Writeln(u"FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, u"Excel.Sheet", MyDir + u"Spreadsheet.xlsx", u"Sheet1!R1C1", true, true);

    // 3 -  A DDEAUTO field:
    builder->Writeln(u"FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, u"Excel.Sheet", MyDir + u"Spreadsheet.xlsx", u"Sheet1!R1C1", true);

    doc->UpdateFields();
    doc->Save(ArtifactsDir + u"Field.LINK.DDE.DDEAUTO.AsImage.docx");
}

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
* Library [Aspose.Words](../../../)
