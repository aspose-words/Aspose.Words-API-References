---
title: get_EpubNavigationMapLevel
second_title: Aspose.Words for C++ API Reference
description: Specifies the maximum level of headings populated to the navigation map when exporting to IDPF EPUB format. Default value is %3.
type: docs
weight: 131
url: /cpp/aspose.words.saving/htmlsaveoptions/get_epubnavigationmaplevel/
---
## HtmlSaveOptions::get_EpubNavigationMapLevel method


Specifies the maximum level of headings populated to the navigation map when exporting to IDPF EPUB format. Default value is **%3**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_EpubNavigationMapLevel() const
```

## Remarks


Navigation map in IDPF EPUB format allows user agents to provide easy way of navigation through the document structure. Usually navigation points correspond to headings in the document. To populate headings up to level **N** assign this value to [EpubNavigationMapLevel](./).

By default, three levels of headings are populated: paragraphs of styles **Heading 1**, **Heading 2** and **Heading 3**. You can set this property to a value from 1 to 9 to request corresponding maximum level. Setting it to zero will reduce navigation map to only document root or roots of document parts.

## Examples



Shows how to filter headings that appear in the navigation panel of a saved Epub document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Every paragraph that we format using a "Heading" style can serve as a heading.
// Each heading may also have a heading level, determined by the number of its heading style.
// The headings below are of levels 1-3.
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// Epub readers typically create a table of contents for their documents.
// Each paragraph with a "Heading" style in the document will create an entry in this table of contents.
// We can use the "EpubNavigationMapLevel" property to set a maximum heading level.
// The Epub reader will not add headings with a level above the one we specify to the contents table.
auto options = MakeObject<HtmlSaveOptions>(SaveFormat::Epub);
options->set_EpubNavigationMapLevel(2);

// Our document has six headings, two of which are above level 2.
// The table of contents for this document will have four entries.
doc->Save(ArtifactsDir + u"HtmlSaveOptions.EpubHeadings.epub", options);
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
