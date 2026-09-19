---
title: "Enum Aspose::Words::Loading::HtmlControlType"
linktitle: "HtmlControlType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::Loading::HtmlControlType. Tipo di nodi del documento che rappresentano gli elementi <input> e <select> importati da HTML in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enum


Tipo di nodi del documento che rappresentano gli elementi <input> e <select> importati da HTML.

```cpp
enum class HtmlControlType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| FormField | 0 | Un campo modulo. |
| StructuredDocumentTag | 1 | Un tag di documento strutturato. |


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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
