---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType metodo"
linktitle: "get_PreferredControlType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType metodo. Ottiene o imposta il tipo preferito di nodi del documento che rappresenteranno gli elementi <input> e <select> importati. Il valore predefinito è FormField in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.loading/htmlloadoptions/get_preferredcontroltype/
---
## HtmlLoadOptions::get_PreferredControlType method


Ottiene o imposta il tipo preferito di nodi del documento che rappresenteranno gli elementi <input> e <select> importati. Il valore predefinito è [FormField](../../htmlcontroltype/).

```cpp
Aspose::Words::Loading::HtmlControlType Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType() const
```


## Esempi



Mostra come impostare il tipo preferito di nodi del documento che rappresenteranno gli elementi <input> e <select> importati.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option value='val1'>item1</option>\r\n                        <option value='val2'></option>\r\n                    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(Aspose::Words::Loading::HtmlControlType::StructuredDocumentTag);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(nodes->idx_get(0));
```

## Vedi anche

* Enum [HtmlControlType](../../htmlcontroltype/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
