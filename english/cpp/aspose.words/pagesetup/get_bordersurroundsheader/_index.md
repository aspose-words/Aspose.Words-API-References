---
title: get_BorderSurroundsHeader
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the page border includes or excludes the header.
type: docs
weight: 92
url: /cpp/aspose.words/pagesetup/get_bordersurroundsheader/
---
## PageSetup::get_BorderSurroundsHeader method


Specifies whether the page border includes or excludes the header.

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsHeader()
```


## Examples



Shows how to apply a border to the page and header/footer. 
```cpp
auto doc = MakeObject<Document>();

auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// Insert a blue double-line border.
SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
// whether a page border surrounds the main body text, also includes the header or footer, respectively.
// Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
// and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(ArtifactsDir + u"PageSetup.PageBorder.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
