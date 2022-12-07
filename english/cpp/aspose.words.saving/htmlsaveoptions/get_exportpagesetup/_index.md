---
title: get_ExportPageSetup
second_title: Aspose.Words for C++ API Reference
description: Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is false.
type: docs
weight: 300
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportpagesetup/
---
## HtmlSaveOptions::get_ExportPageSetup method


Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup() const
```

## Remarks


Each [Section](../../../aspose.words/section/) in Aspose.Words document model provides page setup information via [PageSetup](../../../aspose.words/pagesetup/) class. When you export a document to HTML format you might need to keep this information for further usage. In particular, page setup might be important for rendering to paged media (printing) or subsequent conversion to the native Microsoft Word file formats (DOCX, DOC, RTF, WML).

In most cases HTML is intended for viewing in browsers where pagination is not performed. So this feature is inactive by default.

## Examples



Shows how decide whether to preserve section structure/page setup information when saving to HTML. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TopMargin(36.0);
pageSetup->set_BottomMargin(36.0);
pageSetup->set_PaperSize(PaperSize::A5);

// When saving the document to HTML, we can pass a SaveOptions object
// to decide whether to preserve or discard page setup settings.
// If we set the "ExportPageSetup" flag to "true", the output HTML document will contain our page setup configuration.
// If we set the "ExportPageSetup" flag to "false", the save operation will discard our page setup settings
// for the first section, and both sections will look identical.
auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportPageSetup(exportPageSetup);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.ExportPageSetup.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    ASSERT_TRUE(outDocContents.Contains(String(u"<style type=\"text/css\">") + u"@page Section1 { size:419.55pt 595.3pt; margin:36pt 70.85pt }" +
                                        u"@page Section2 { size:612pt 792pt; margin:70.85pt }" +
                                        u"div.Section1 { page:Section1 }div.Section2 { page:Section2 }" + u"</style>"));

    ASSERT_TRUE(outDocContents.Contains(String(u"<div class=\"Section1\">") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                                        u"<span>Section 1</span>" + u"</p>" + u"</div>"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));

    ASSERT_TRUE(outDocContents.Contains(String(u"<div>") + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Section 1</span>" + u"</p>" +
                                        u"</div>"));
}
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
