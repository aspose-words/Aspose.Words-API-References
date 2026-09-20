---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType método"
linktitle: "get_PreferredControlType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType método. Obtiene o establece el tipo preferido de nodos de documento que representarán los elementos <input> y <select> importados. El valor predeterminado es FormField en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.loading/htmlloadoptions/get_preferredcontroltype/
---
## HtmlLoadOptions::get_PreferredControlType method


Obtiene o establece el tipo preferido de nodos de documento que representarán los elementos <input> y <select> importados. El valor predeterminado es [FormField](../../htmlcontroltype/).

```cpp
Aspose::Words::Loading::HtmlControlType Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType() const
```


## Ejemplos



Muestra cómo establecer el tipo preferido de nodos de documento que representarán los elementos <input> y <select> importados.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option value='val1'>item1</option>\r\n                        <option value='val2'></option>\r\n                    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(Aspose::Words::Loading::HtmlControlType::StructuredDocumentTag);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(nodes->idx_get(0));
```

## Ver también

* Enum [HtmlControlType](../../htmlcontroltype/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
