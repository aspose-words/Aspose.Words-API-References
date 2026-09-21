---
title: "Aspose::Words::Loading::HtmlControlType enum"
linktitle: "HtmlControlType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::HtmlControlType enum. Typ av dokumentnoder som representerar <input>- och <select>-element importerade från HTML i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enum


Typ av dokumentnoder som representerar <input>- och <select>-element som importeras från HTML.

```cpp
enum class HtmlControlType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| FormField | 0 | Ett formulärfält. |
| StructuredDocumentTag | 1 | En strukturerad dokumenttagg. |


## Exempel



Visar hur man anger föredragen typ av dokumentnoder som ska representera importerade <input>- och <select>-element.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option value='val1'>item1</option>\r\n                        <option value='val2'></option>\r\n                    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(Aspose::Words::Loading::HtmlControlType::StructuredDocumentTag);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(nodes->idx_get(0));
```

## Se även

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
