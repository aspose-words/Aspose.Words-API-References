---
title: "enumeración Aspose::Words::Loading::HtmlControlType"
linktitle: "HtmlControlType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "enumeración Aspose::Words::Loading::HtmlControlType. Tipo de nodos de documento que representan los elementos <input> y <select> importados desde HTML en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enum


Tipo de nodos de documento que representan los elementos <input> y <select> importados desde HTML.

```cpp
enum class HtmlControlType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| FormField | 0 | Un campo de formulario. |
| StructuredDocumentTag | 1 | Una etiqueta de documento estructurado. |


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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
