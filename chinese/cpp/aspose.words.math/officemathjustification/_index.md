---
title: "Aspose::Words::Math::OfficeMathJustification enum"
linktitle: "OfficeMathJustification"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Math::OfficeMathJustification 枚举。指定 C++ 中方程式的对齐方式。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enum


指定等式的对齐方式。

```cpp
enum class OfficeMathJustification
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| CenterGroup | 1 | 将数学文本实例相互之间左对齐，并将数学文本组（[Math](../)[Paragraph](../../aspose.words/paragraph/)）在页面上居中。 |
| 居中 | 2 | 将每个数学文本实例相对于页边距单独居中。 |
| Left | 3 | 左对齐 [Math](../)[Paragraph](../../aspose.words/paragraph/)。 |
| Right | 4 | 右对齐 [Math](../)[Paragraph](../../aspose.words/paragraph/)。 |
| Inline | 7 | [Inline](../../aspose.words/inline/) 位置的 [Math](../)。 |
| Default | n/a | 默认值为 [CenterGroup](./)。 |


## 示例



展示如何设置 Office Math 显示格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// OfficeMath 节点如果是其他 OfficeMath 节点的子节点，则始终以内联方式呈现。
// 我们正在处理的节点是基节点，用于更改其位置和显示类型。
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// 更改 OfficeMath 节点的位置和显示类型。
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## 另见

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
