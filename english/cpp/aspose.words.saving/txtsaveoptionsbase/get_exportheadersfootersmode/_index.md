---
title: get_ExportHeadersFootersMode
second_title: Aspose.Words for C++ API Reference
description: Specifies the way headers and footers are exported to the text formats. Default value is PrimaryOnly.
type: docs
weight: 40
url: /cpp/aspose.words.saving/txtsaveoptionsbase/get_exportheadersfootersmode/
---
## TxtSaveOptionsBase::get_ExportHeadersFootersMode method


Specifies the way headers and footers are exported to the text formats. Default value is [PrimaryOnly](../../txtexportheadersfootersmode/).

```cpp
Aspose::Words::Saving::TxtExportHeadersFootersMode Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode() const
```


## Examples



Shows how to specify how to export headers and footers to plain text format. 
```cpp
auto doc = MakeObject<Document>();

// Insert even and primary headers/footers into the document.
// The primary header/footers will override the even headers/footers.
doc->get_FirstSection()->get_HeadersFooters()->Add(MakeObject<HeaderFooter>(doc, HeaderFooterType::HeaderEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::HeaderEven)->AppendParagraph(u"Even header");
doc->get_FirstSection()->get_HeadersFooters()->Add(MakeObject<HeaderFooter>(doc, HeaderFooterType::FooterEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::FooterEven)->AppendParagraph(u"Even footer");
doc->get_FirstSection()->get_HeadersFooters()->Add(MakeObject<HeaderFooter>(doc, HeaderFooterType::HeaderPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::HeaderPrimary)->AppendParagraph(u"Primary header");
doc->get_FirstSection()->get_HeadersFooters()->Add(MakeObject<HeaderFooter>(doc, HeaderFooterType::FooterPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::FooterPrimary)->AppendParagraph(u"Primary footer");

// Insert pages to display these headers and footers.
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Page 1");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(BreakType::PageBreak);
builder->Write(u"Page 3");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
auto saveOptions = MakeObject<TxtSaveOptions>();

// Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.None"
// to not export any headers/footers.
// Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.PrimaryOnly"
// to only export primary headers/footers.
// Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.AllAtEnd"
// to place all headers and footers for all section bodies at the end of the document.
saveOptions->set_ExportHeadersFootersMode(txtExportHeadersFootersMode);

doc->Save(ArtifactsDir + u"TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

String docText = System::IO::File::ReadAllText(ArtifactsDir + u"TxtSaveOptions.ExportHeadersFooters.txt");

switch (txtExportHeadersFootersMode)
{
case TxtExportHeadersFootersMode::AllAtEnd:
    ASSERT_EQ(String(u"Page 1\r\n") + u"Page 2\r\n" + u"Page 3\r\n" + u"Even header\r\n\r\n" + u"Primary header\r\n\r\n" + u"Even footer\r\n\r\n" +
                  u"Primary footer\r\n\r\n",
              docText);
    break;

case TxtExportHeadersFootersMode::PrimaryOnly:
    ASSERT_EQ(String(u"Primary header\r\n") + u"Page 1\r\n" + u"Page 2\r\n" + u"Page 3\r\n" + u"Primary footer\r\n", docText);
    break;

case TxtExportHeadersFootersMode::None:
    ASSERT_EQ(String(u"Page 1\r\n") + u"Page 2\r\n" + u"Page 3\r\n", docText);
    break;
}
```

## See Also

* Enum [TxtExportHeadersFootersMode](../../txtexportheadersfootersmode/)
* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
