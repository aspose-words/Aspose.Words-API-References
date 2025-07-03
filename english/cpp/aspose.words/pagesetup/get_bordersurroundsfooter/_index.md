---
title: Aspose::Words::PageSetup::get_BorderSurroundsFooter method
linktitle: get_BorderSurroundsFooter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_BorderSurroundsFooter method. Specifies whether the page border includes or excludes the footer in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/pagesetup/get_bordersurroundsfooter/
---
## PageSetup::get_BorderSurroundsFooter method


Specifies whether the page border includes or excludes the footer.

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsFooter()
```


## Examples



Shows how to apply a border to the page and header/footer. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// Insert a blue double-line border.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
// whether a page border surrounds the main body text, also includes the header or footer, respectively.
// Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
// and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorder.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
