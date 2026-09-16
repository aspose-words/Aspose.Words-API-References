---
title: "Aspose::Words::Math::OfficeMath::get_NodeType 方法"
linktitle: "get_NodeType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Math::OfficeMath::get_NodeType 方法。返回 OfficeMath（在 C++ 中）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.math/officemath/get_nodetype/
---
## OfficeMath::get_NodeType method


返回 [OfficeMath](../../../aspose.words/nodetype/)。

```cpp
Aspose::Words::NodeType Aspose::Words::Math::OfficeMath::get_NodeType() const override
```


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

* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
