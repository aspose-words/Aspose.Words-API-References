---
title: get_ExportCidUrlsForMhtmlResources
second_title: Aspose.Words for C++ API Reference
description: Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is false.
type: docs
weight: 157
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportcidurlsformhtmlresources/
---
## HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method


Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources() const
```

## Remarks


This option affects only documents being saved to MHTML.

By default, resources in MHTML documents are referenced by file name (for example, "image.png"), which are matched against "Content-Location" headers of MIME parts.

This option enables an alternative method, where references to resource files are written as CID (Content-ID) URLs (for example, "cid:image.png") and are matched against "Content-ID" headers.

In theory, there should be no difference between the two referencing methods and either of them should work fine in any browser or mail agent. In practice, however, some agents fail to fetch resources by file name. If your browser or mail agent refuses to load resources included in an MTHML document (doesn't show images or doesn't load CSS styles), try exporting the document with CID URLs.

## Examples



Shows how to enable content IDs for output MHTML documents. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Setting this flag will replace "Content-Location" tags
// with "Content-ID" tags for each resource from the input document.
auto options = MakeObject<HtmlSaveOptions>(SaveFormat::Mhtml);
options->set_ExportCidUrlsForMhtmlResources(exportCidUrlsForMhtmlResources);
options->set_CssStyleSheetType(CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_PrettyFormat(true);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.ContentIdUrls.mht", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-ID: <document.html>"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; src:url('cid:ariblk.ttf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-Location: document.html"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; src:url('ariblk.ttf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
