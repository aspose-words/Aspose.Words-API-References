---
title: get_Text
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the text that will be inserted into the document for the current merge field.
type: docs
weight: 1
url: /cpp/aspose.words.mailmerging/fieldmergingargs/get_text/
---
## FieldMergingArgs::get_Text method


Gets or sets the text that will be inserted into the document for the current merge field.

```cpp
System::String Aspose::Words::MailMerging::FieldMergingArgs::get_Text() const
```

## Remarks


When your event handler is called, this property is set to null.

If you leave Text as null, the mail merge engine will insert [FieldValue](../../fieldmergingargsbase/get_fieldvalue/) in place of the merge field.

If you set Text to any string (including empty), the string will be inserted into the document in place of the merge field.

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

* Class [FieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words](../../../)
