---
title: Aspose::Words::Math::OfficeMathDisplayType enum
linktitle: OfficeMathDisplayType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Math::OfficeMathDisplayType enum. Specifies the display format type of the equation in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enum


Specifies the display format type of the equation.

```cpp
enum class OfficeMathDisplayType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Display | 0 | The Office [Math](../) is displayed on its own line. |
| Inline | 1 | The Office [Math](../) is displayed inline with the text. |


## Examples



Shows how to set office math display formatting. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// OfficeMath nodes that are children of other OfficeMath nodes are always inline.
// The node we are working with is the base node to change its location and display type.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// Change the location and display type of the OfficeMath node.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## See Also

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
