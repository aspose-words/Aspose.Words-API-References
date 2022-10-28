---
title: get_PreferredControlType
second_title: Aspose.Words for C++ API Reference
description: Gets or sets preferred type of document nodes that will represent imported <input> and <select> elements. Default value is FormField.
type: docs
weight: 53
url: /cpp/aspose.words.loading/htmlloadoptions/get_preferredcontroltype/
---
## HtmlLoadOptions.get_PreferredControlType method


Gets or sets preferred type of document nodes that will represent imported <input> and <select> elements. Default value is **FormField**.

```cpp
Aspose::Words::Loading::HtmlControlType Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType() const
```


## Examples




Shows how to set preferred type of document nodes that will represent imported <input> and <select> elements. 
```cpp
const String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option "
                    u"value='val1'>item1</option>\r\n                        <option value='val2'></option>                        \r\n                "
                    u"    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = MakeObject<HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(HtmlControlType::StructuredDocumentTag);

auto doc = MakeObject<Document>(MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
SharedPtr<NodeCollection> nodes = doc->GetChildNodes(NodeType::StructuredDocumentTag, true);

auto tag = System::DynamicCast<StructuredDocumentTag>(nodes->idx_get(0));
```

