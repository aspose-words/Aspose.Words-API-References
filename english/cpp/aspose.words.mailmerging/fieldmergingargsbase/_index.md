---
title: FieldMergingArgsBase
second_title: Aspose.Words for C++ API Reference
description: Base class for FieldMergingArgs and ImageFieldMergingArgs.
type: docs
weight: 14
url: /cpp/aspose.words.mailmerging/fieldmergingargsbase/
---
## FieldMergingArgsBase class


Base class for [FieldMergingArgs](../fieldmergingargs/) and [ImageFieldMergingArgs](../imagefieldmergingargs/).

```cpp
class FieldMergingArgsBase : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Document](./get_document/)() const | Returns the [Document](./get_document/) object for which the mail merge is performed. |
| [get_DocumentFieldName](./get_documentfieldname/)() const | Gets the name of the merge field as specified in the document. |
| [get_Field](./get_field/)() const | Gets the object that represents the current merge field. |
| [get_FieldName](./get_fieldname/)() const | Gets the name of the merge field in the data source. |
| [get_FieldValue](./get_fieldvalue/)() const | Gets the value of the field from the data source. |
| [get_RecordIndex](./get_recordindex/)() const | Gets the zero based index of the record that is being merged. |
| [get_TableName](./get_tablename/)() const | Gets the name of the data table for the current merge operation or empty string if the name is not available. |
| [set_FieldValue](./set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Sets the value of the field from the data source. |

## Examples




Shows how to execute a mail merge with a custom callback that handles merge data in the form of HTML documents. 
```cpp
void MergeHtml()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->InsertField(u"MERGEFIELD  html_Title  \\b Content");
    builder->InsertField(u"MERGEFIELD  html_Body  \\b Content");

    ArrayPtr<SharedPtr<System::Object>> mergeData = MakeArray<SharedPtr<System::Object>>(
        {System::ObjectExt::Box<String>(String(u"<html>") + u"<h1>" + u"<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
                                        u"</h1>" + u"</html>"),
         System::ObjectExt::Box<String>(
             String(u"<html>") + u"<blockquote>" +
             u"<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
             u"</blockquote>" + u"</html>")});

    doc->get_MailMerge()->set_FieldMergingCallback(MakeObject<ExMailMergeEvent::HandleMergeFieldInsertHtml>());
    doc->get_MailMerge()->Execute(MakeArray<String>({u"html_Title", u"html_Body"}), mergeData);

    doc->Save(ArtifactsDir + u"MailMergeEvent.MergeHtml.docx");
}

class HandleMergeFieldInsertHtml : public IFieldMergingCallback
{
private:
    void FieldMerging(SharedPtr<FieldMergingArgs> args) override
    {
        if (args->get_DocumentFieldName().StartsWith(u"html_") && args->get_Field()->GetFieldCode().Contains(u"\\b"))
        {
            // Add parsed HTML data to the document's body.
            auto builder = MakeObject<DocumentBuilder>(args->get_Document());
            builder->MoveToMergeField(args->get_DocumentFieldName());
            builder->InsertHtml(System::ObjectExt::Unbox<String>(args->get_FieldValue()));

            // Since we have already inserted the merged content manually,
            // we will not need to respond to this event by returning content via the "Text" property.
            args->set_Text(String::Empty);
        }
    }

    void ImageFieldMerging(SharedPtr<ImageFieldMergingArgs> args) override
    {
        // Do nothing.
    }
};
```

