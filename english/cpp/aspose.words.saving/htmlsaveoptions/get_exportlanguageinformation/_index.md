---
title: Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation method
linktitle: get_ExportLanguageInformation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation method. Specifies whether language information is exported to HTML, MHTML or EPUB. Default is false in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportlanguageinformation/
---
## HtmlSaveOptions::get_ExportLanguageInformation method


Specifies whether language information is exported to HTML, MHTML or EPUB. Default is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation() const
```

## Remarks


When this property is set to **true** Aspose.Words outputs **lang** HTML attribute on the document elements that specify language. This can be needed to preserve language related semantics.

## Examples



Shows how to preserve language information when saving to .html. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Use the builder to write text while formatting it in different locales.
builder->get_Font()->set_LocaleId(MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID());
builder->Writeln(u"Hello world!");

builder->get_Font()->set_LocaleId(MakeObject<System::Globalization::CultureInfo>(u"en-GB")->get_LCID());
builder->Writeln(u"Hello again!");

builder->get_Font()->set_LocaleId(MakeObject<System::Globalization::CultureInfo>(u"ru-RU")->get_LCID());
builder->Write(u"Привет, мир!");

// When saving the document to HTML, we can pass a SaveOptions object
// to either preserve or discard each formatted text's locale.
// If we set the "ExportLanguageInformation" flag to "true",
// the output HTML document will contain the locales in "lang" attributes of <span> tags.
// If we set the "ExportLanguageInformation" flag to "false',
// the text in the output HTML document will not contain any locale information.
auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportLanguageInformation(exportLanguageInformation);
options->set_PrettyFormat(true);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.ExportLanguageInformation.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"en-GB\">Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Привет, мир!</span>"));
}
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
