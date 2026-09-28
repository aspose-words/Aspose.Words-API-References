---
title: "Перечисление Aspose::Words::Loading::HtmlControlType"
linktitle: "HtmlControlType"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Loading::HtmlControlType. Тип узлов документа, представляющих элементы <input> и <select>, импортированные из HTML в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enum


Тип узлов документа, представляющих элементы <input> и <select>, импортированные из HTML.

```cpp
enum class HtmlControlType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| FormField | 0 | Поле формы. |
| StructuredDocumentTag | 1 | Структурированный тег документа. |


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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
