---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType metod"
linktitle: "get_PreferredControlType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType metod. Hämtar eller anger föredragen typ av dokumentnoder som kommer att representera importerade <input>- och <select>-element. Standardvärdet är FormField i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.loading/htmlloadoptions/get_preferredcontroltype/
---
## HtmlLoadOptions::get_PreferredControlType method


Hämtar eller anger föredragen typ av dokumentnoder som kommer att representera importerade <input>- och <select>-element. Standardvärdet är [FormField](../../htmlcontroltype/).

```cpp
Aspose::Words::Loading::HtmlControlType Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType() const
```


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

* Enum [HtmlControlType](../../htmlcontroltype/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
