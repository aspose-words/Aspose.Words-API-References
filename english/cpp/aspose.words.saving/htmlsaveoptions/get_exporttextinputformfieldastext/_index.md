---
title: get_ExportTextInputFormFieldAsText
second_title: Aspose.Words for C++ API Reference
description: Controls how text input form fields are saved to HTML or MHTML. Default value is false.
type: docs
weight: 339
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exporttextinputformfieldastext/
---
## HtmlSaveOptions::get_ExportTextInputFormFieldAsText method


Controls how text input form fields are saved to HTML or MHTML. Default value is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText() const
```

## Remarks


When set to **true**, exports text input form fields as normal text. When **false**, exports Word text input form fields as INPUT elements in HTML.

When exporting to EPUB, text input form fields are always saved as text due to requirements of this format.

## Examples



Shows how to specify the folder for storing linked images after saving to .html. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

String imagesDir = System::IO::Path::Combine(ArtifactsDir, u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Set an option to export form fields as plain text instead of HTML input elements.
auto options = MakeObject<HtmlSaveOptions>(SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
