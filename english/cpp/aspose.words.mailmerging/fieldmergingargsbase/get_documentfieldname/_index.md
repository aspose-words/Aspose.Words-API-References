---
title: Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName method
linktitle: get_DocumentFieldName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName method. Gets the name of the merge field as specified in the document in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.mailmerging/fieldmergingargsbase/get_documentfieldname/
---
## FieldMergingArgsBase::get_DocumentFieldName method


Gets the name of the merge field as specified in the document.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgsBase::get_DocumentFieldName() const
```

## Remarks


If you have a mapping from a document field name to a different data source field name, then this is the original field name as specified in the document.

If you specified a field name prefix, for example "Image:MyFieldName" in the document, then [DocumentFieldName](./) returns field name without the prefix, that is "MyFieldName".

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

## See Also

* Class [FieldMergingArgsBase](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
