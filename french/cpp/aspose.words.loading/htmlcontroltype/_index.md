---
title: "Aspose::Words::Loading::HtmlControlType énumération"
linktitle: "HtmlControlType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::HtmlControlType énumération. Type de nœuds de document qui représentent les éléments <input> et <select> importés depuis le HTML en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enum


Type de nœuds de document qui représentent les éléments <input> et <select> importés depuis HTML.

```cpp
enum class HtmlControlType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| FormField | 0 | Un champ de formulaire. |
| StructuredDocumentTag | 1 | Une balise de document structurée. |


## Exemples



Montre comment définir le type préféré des nœuds de document qui représenteront les éléments <input> et <select> importés.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option value='val1'>item1</option>\r\n                        <option value='val2'></option>\r\n                    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(Aspose::Words::Loading::HtmlControlType::StructuredDocumentTag);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(nodes->idx_get(0));
```

## Voir aussi

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
