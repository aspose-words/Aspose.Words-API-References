---
title: "Aspose::Words::Loading::HtmlControlType 枚举"
linktitle: "HtmlControlType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::HtmlControlType 枚举。表示从 HTML 导入的 <input> 和 <select> 元素的文档节点类型（C++）。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enum


表示从 HTML 导入的 <input> 和 <select> 元素的文档节点类型。

```cpp
enum class HtmlControlType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| FormField | 0 | 表单字段。 |
| StructuredDocumentTag | 1 | 结构化文档标签。 |


## 示例



展示如何设置将表示导入的 <input> 和 <select> 元素的文档节点的首选类型。
```cpp
const System::String html = u"\r\n                <html>\r\n                    <select name='ComboBox' size='1'>\r\n                        <option value='val1'>item1</option>\r\n                        <option value='val2'></option>\r\n                    </select>\r\n                </html>\r\n            ";

auto htmlLoadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
htmlLoadOptions->set_PreferredControlType(Aspose::Words::Loading::HtmlControlType::StructuredDocumentTag);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), htmlLoadOptions);
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(nodes->idx_get(0));
```

## 另见

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
