---
title: Aspose::Words::Loading::BlockImportMode enum
linktitle: BlockImportMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::BlockImportMode enum. Specifies how properties of block-level elements are imported from HTML-based documents in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.loading/blockimportmode/
---
## BlockImportMode enum


Specifies how properties of block-level elements are imported from HTML-based documents.

```cpp
enum class BlockImportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Merge | 0 | [Properties](../../aspose.words.properties/) of parent blocks are merged and stored on child elements (i.e. paragraphs or tables). |
| Preserve | 1 | [Properties](../../aspose.words.properties/) of parent blocks are imported to a special logical structure and are stored separately from document nodes. |


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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
