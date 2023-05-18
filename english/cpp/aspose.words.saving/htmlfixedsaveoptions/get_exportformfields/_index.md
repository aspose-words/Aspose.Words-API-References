---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields method
linktitle: get_ExportFormFields
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields method. Gets or sets indication of whether form fields are exported as interactive items (as ''input'' tag) rather than converted to text or graphics in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportformfields/
---
## HtmlFixedSaveOptions::get_ExportFormFields method


Gets or sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields() const
```


## Examples



Shows how to export form fields to Html. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->InsertCheckBox(u"CheckBox", false, 15);

// When we export a document with form fields to .html,
// there are two ways in which Aspose.Words can export form fields.
// Setting the "ExportFormFields" flag to "true" will export them as interactive objects.
// Setting this flag to "false" will display form fields as plain text.
// This will freeze them at their current value, and prevent the reader of our HTML document
// from being able to interact with them.
auto htmlFixedSaveOptions = MakeObject<HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportFormFields(exportFormFields);

doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(
                    outDocContents, String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") +
                                        u"<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />")
                    ->get_Success());
}
else
{
    ASSERT_TRUE(
        System::Text::RegularExpressions::Regex::Match(
            outDocContents, String(u"<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>") +
                                u"<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"")
            ->get_Success());
}
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
