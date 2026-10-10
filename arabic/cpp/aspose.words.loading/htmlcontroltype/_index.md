---
title: "تعداد Aspose::Words::Loading::HtmlControlType"
linktitle: "HtmlControlType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Loading::HtmlControlType. نوع عقد المستند التي تمثل عناصر <input> و <select> المستوردة من HTML في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enum


نوع عقد المستند التي تمثل عناصر <input> و <select> المستوردة من HTML.

```cpp
enum class HtmlControlType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| FormField | 0 | حقل نموذج. |
| StructuredDocumentTag | 1 | علامة مستند مُنظمة. |


## أمثلة



يوضح كيفية تعيين النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة <input> و <select>.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option value='val1'>item1</option>\r\n                        <option value='val2'></option>\r\n                    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(Aspose::Words::Loading::HtmlControlType::StructuredDocumentTag);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(nodes->idx_get(0));
```

## انظر أيضًا

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
