---
title: "Aspose::Words::Markup::SdtAppearance 枚举"
linktitle: "SdtAppearance"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::SdtAppearance 枚举. 指定 C++ 中结构化文档标签的外观。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.markup/sdtappearance/
---
## SdtAppearance enum


指定结构化文档标签的外观。

```cpp
enum class SdtAppearance
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| BoundingBox | 0 | 表示显示为阴影矩形或边界框的结构化文档标签。 |
| Tags | 1 | 表示显示为起始和结束标记的结构化文档标签。 |
| Hidden | 2 | 表示一个未显示的结构化文档标签。 |
| Default | n/a | 默认是 [BoundingBox](./)。 |


## 示例



展示如何在内容周围显示标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## 另见

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
