---
title: Aspose::Words::HtmlInsertOptions enum
linktitle: HtmlInsertOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::HtmlInsertOptions enum. Specifies options for the InsertHtml() method in C++.'
type: docs
weight: 92000
url: /cpp/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enum


Specifies options for the [InsertHtml()](../) method.

```cpp
enum class HtmlInsertOptions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | Use the default options when inserting HTML. |
| UseBuilderFormatting | 1 | Use font and paragraph formatting specified in [DocumentBuilder](../documentbuilder/) as base formatting for text inserted from HTML. |
| RemoveLastEmptyParagraph | 2 | Remove the empty paragraph that is normally inserted after HTML that ends with a block-level element. |
| PreserveBlocks | 4 | Preserve properties of block-level elements. |


## Examples



Shows how to allows better preserve borders and margins seen. 
```cpp
const System::String html = u"\r\n                <html>\r\n                    <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                    </div>\r\n                </html>";

// Set the new mode of import HTML block-level elements.
Aspose::Words::HtmlInsertOptions insertOptions = Aspose::Words::HtmlInsertOptions::PreserveBlocks;

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
builder->InsertHtml(html, insertOptions);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.PreserveBlocks.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
