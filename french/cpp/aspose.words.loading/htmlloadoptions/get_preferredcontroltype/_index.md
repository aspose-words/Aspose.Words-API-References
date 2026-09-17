---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType méthode"
linktitle: "get_PreferredControlType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType méthode. Obtient ou définit le type préféré des nœuds de document qui représenteront les éléments <input> et <select> importés. La valeur par défaut est FormField en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.loading/htmlloadoptions/get_preferredcontroltype/
---
## HtmlLoadOptions::get_PreferredControlType method


Obtient ou définit le type préféré des nœuds de document qui représenteront les éléments <input> et <select> importés. La valeur par défaut est [FormField](../../htmlcontroltype/).

```cpp
Aspose::Words::Loading::HtmlControlType Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType() const
```


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

* Enum [HtmlControlType](../../htmlcontroltype/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
