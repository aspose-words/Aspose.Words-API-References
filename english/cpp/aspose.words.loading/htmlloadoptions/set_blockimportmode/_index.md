---
title: Aspose::Words::Loading::HtmlLoadOptions::set_BlockImportMode method
linktitle: set_BlockImportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::HtmlLoadOptions::set_BlockImportMode method. Sets a value that specifies how properties of block-level elements are imported. Default value is Merge in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.loading/htmlloadoptions/set_blockimportmode/
---
## HtmlLoadOptions::set_BlockImportMode method


Sets a value that specifies how properties of block-level elements are imported. Default value is [Merge](../../blockimportmode/).

```cpp
void Aspose::Words::Loading::HtmlLoadOptions::set_BlockImportMode(Aspose::Words::Loading::BlockImportMode value)
```

## Examples


Shows how properties of block-level elements are imported from HTML-based documents.

```cpp
const System::String html = u"\r\n            <html>\r\n                <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                </div>\r\n            </html>";
auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html));

auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
// Set the new mode of import HTML block-level elements.
loadOptions->set_BlockImportMode(blockImportMode);

auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BlockImport.docx");
```
## See Also

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
