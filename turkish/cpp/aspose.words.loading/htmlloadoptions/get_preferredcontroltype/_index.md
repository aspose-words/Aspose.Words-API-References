---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType metodu"
linktitle: "get_PreferredControlType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType metodu. Alır veya ayarlar içe aktarılan <input> ve <select> öğelerini temsil edecek belge düğümlerinin tercih edilen türünü. Varsayılan değer C++'de FormField."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.loading/htmlloadoptions/get_preferredcontroltype/
---
## HtmlLoadOptions::get_PreferredControlType method


Alır veya ayarlar içe aktarılan <input> ve <select> öğelerini temsil edecek belge düğümlerinin tercih edilen türünü. Varsayılan değer [FormField](../../htmlcontroltype/).

```cpp
Aspose::Words::Loading::HtmlControlType Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType() const
```


## Örnekler



İçe aktarılan <input> ve <select> öğelerini temsil edecek belge düğümlerinin tercih edilen türünün nasıl ayarlanacağını gösterir.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option value='val1'>item1</option>\r\n                        <option value='val2'></option>\r\n                    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(Aspose::Words::Loading::HtmlControlType::StructuredDocumentTag);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(nodes->idx_get(0));
```

## Ayrıca Bakınız

* Enum [HtmlControlType](../../htmlcontroltype/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
