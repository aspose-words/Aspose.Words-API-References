---
title: get_ExportDropDownFormFieldAsText
second_title: Aspose.Words for C++ API Reference
description: Controls how drop-down form fields are saved to HTML or MHTML. Default value is false.
type: docs
weight: 170
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportdropdownformfieldastext/
---
## HtmlSaveOptions::get_ExportDropDownFormFieldAsText method


Controls how drop-down form fields are saved to HTML or MHTML. Default value is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText() const
```

## Remarks


When set to **true**, exports drop-down form fields as normal text. When **false**, exports drop-down form fields as SELECT element in HTML.

When exporting to EPUB, text drop-down form fields are always saved as text due to requirements of this format.

## Examples



Shows how to get drop-down combo box form fields to blend in with paragraph text when saving to html. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Use a document builder to insert a combo box with the value "Two" selected.
builder->InsertComboBox(u"MyComboBox", MakeArray<String>({u"One", u"Two", u"Three"}), 1);

// The "ExportDropDownFormFieldAsText" flag of this SaveOptions object allows us to
// control how saving the document to HTML treats drop-down combo boxes.
// Setting it to "true" will convert each combo box into simple text
// that displays the combo box's currently selected value, effectively freezing it.
// Setting it to "false" will preserve the functionality of the combo box using <select> and <option> tags.
auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.DropDownFormField.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Two</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(String(u"<select name=\"MyComboBox\">") + u"<option>One</option>" +
                                        u"<option selected=\"selected\">Two</option>" + u"<option>Three</option>" + u"</select>"));
}
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
