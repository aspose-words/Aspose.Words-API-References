---
title: "Aspose::Words::Loading::HtmlControlType enum"
linktitle: "HtmlControlType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::HtmlControlType enum. Typ von Dokumentknoten, die <input>- und <select>-Elemente darstellen, die aus HTML in C++ importiert wurden."
type: docs
weight: 15000
url: /de/cpp/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enum


Typ von Dokumentknoten, die <input>- und <select>-Elemente darstellen, die aus HTML importiert wurden.

```cpp
enum class HtmlControlType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| FormField | 0 | Ein Formularfeld. |
| StructuredDocumentTag | 1 | Ein strukturiertes Dokument-Tag. |


## Beispiele



Zeigt, wie man den bevorzugten Typ von Dokumentknoten festlegt, die importierte <input>- und <select>-Elemente darstellen.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option value='val1'>item1</option>\r\n                        <option value='val2'></option>\r\n                    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(Aspose::Words::Loading::HtmlControlType::StructuredDocumentTag);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(nodes->idx_get(0));
```

## Siehe auch

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
