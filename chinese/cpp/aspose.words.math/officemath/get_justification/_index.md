---
title: "Aspose::Words::Math::OfficeMath::get_Justification 方法"
linktitle: "get_Justification"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Math::OfficeMath::get_Justification 方法。在 C++ 中获取/设置 Office Math 对齐方式。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.math/officemath/get_justification/
---
## OfficeMath::get_Justification method


获取/设置 Office [Math](../../) 对齐方式。

```cpp
Aspose::Words::Math::OfficeMathJustification Aspose::Words::Math::OfficeMath::get_Justification()
```

## 备注


无法将对齐方式设置为显示格式类型为 [Inline](../../officemathdisplaytype/) 的 Office [Math](../../)。

[Inline](../../../aspose.words/inline/) justification cannot be set to the Office [Math](../../) with display format type [Display](../../officemathdisplaytype/).

在设置 Office [Math](../../) 对齐方式之前，必须先设置相应的 [DisplayType](../get_displaytype/)。

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

* Enum [OfficeMathJustification](../../officemathjustification/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
