---
title: "Метод Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType"
linktitle: "get_PreferredControlType"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType. Получает или задает предпочтительный тип узлов документа, которые будут представлять импортированные элементы <input> и <select>. Значение по умолчанию — FormField в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.loading/htmlloadoptions/get_preferredcontroltype/
---
## HtmlLoadOptions::get_PreferredControlType method


Получает или задает предпочтительный тип узлов документа, которые будут представлять импортированные элементы <input> и <select>. Значение по умолчанию — [FormField](../../htmlcontroltype/).

```cpp
Aspose::Words::Loading::HtmlControlType Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType() const
```


## Примеры



Показывает, как задать предпочтительный тип узлов документа, которые будут представлять импортированные элементы <input> и <select>.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option value='val1'>item1</option>\r\n                        <option value='val2'></option>\r\n                    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(Aspose::Words::Loading::HtmlControlType::StructuredDocumentTag);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(nodes->idx_get(0));
```

## См. также

* Enum [HtmlControlType](../../htmlcontroltype/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
