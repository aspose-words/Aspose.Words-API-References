---
title: Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion method
linktitle: get_HtmlVersion
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion method. Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is Xhtml in C++.'
type: docs
weight: 35000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_htmlversion/
---
## HtmlSaveOptions::get_HtmlVersion method


Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is [Xhtml](../../htmlversion/).

```cpp
Aspose::Words::Saving::HtmlVersion Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion() const
```


## Examples



Shows how to save a document to a specific version of HTML. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

auto options = MakeObject<HtmlSaveOptions>(SaveFormat::Html);
options->set_HtmlVersion(htmlVersion);
options->set_PrettyFormat(true);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.HtmlVersions.html", options);

// Our HTML documents will have minor differences to be compatible with different HTML versions.
String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
case HtmlVersion::Html5:
    ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
    ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
    break;

case HtmlVersion::Xhtml:
    ASSERT_TRUE(outDocContents.Contains(u"<a name=\"_Toc76372689\"></a>"));
    ASSERT_TRUE(outDocContents.Contains(u"<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; "
                                        u"-aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
    break;
}
```


Shows how to display a DOCTYPE heading when converting documents to the Xhtml 1.0 transitional standard. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = MakeObject<HtmlSaveOptions>(SaveFormat::Html);
options->set_HtmlVersion(HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Our document will only contain a DOCTYPE declaration heading if we have set the "ExportXhtmlTransitional" flag to "true".
String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.ExportXhtmlTransitional.html");

if (showDoctypeDeclaration)
{
    ASSERT_TRUE(outDocContents.Contains(String(u"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n") +
                                        u"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" "
                                        u"\"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
                                        u"<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<html>"));
}
```

## See Also

* Enum [HtmlVersion](../../htmlversion/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
