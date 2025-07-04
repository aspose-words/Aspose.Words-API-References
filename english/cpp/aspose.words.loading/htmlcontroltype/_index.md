---
title: Aspose::Words::Loading::HtmlControlType enum
linktitle: HtmlControlType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::HtmlControlType enum. Type of document nodes that represent <input> and <select> elements imported from HTML in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enum


Type of document nodes that represent <input> and <select> elements imported from HTML.

```cpp
enum class HtmlControlType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| FormField | 0 | A form field. |
| StructuredDocumentTag | 1 | A structured document tag. |


## Examples



Shows how to set preferred type of document nodes that will represent imported <input> and <select> elements. 
```cpp
const System::String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option value='val1'>item1</option>\r\n                        <option value='val2'></option>\r\n                    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(Aspose::Words::Loading::HtmlControlType::StructuredDocumentTag);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(nodes->idx_get(0));
```

## See Also

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
