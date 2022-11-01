---
title: get_Justification
second_title: Aspose.Words for C++ API Reference
description: Gets/sets Office Math justification.
type: docs
weight: 40
url: /cpp/aspose.words.math/officemath/get_justification/
---
## OfficeMath.get_Justification method


Gets/sets Office [Math](../../) justification.

```cpp
Aspose::Words::Math::OfficeMathJustification Aspose::Words::Math::OfficeMath::get_Justification()
```


Justification cannot be set to the Office [Math](../../) with display format type **Inline**.

[Inline](../../../aspose.words/inline/) justification cannot be set to the Office [Math](../../) with display format type **Display**.

Corresponding [DisplayType](../get_displaytype/) has to be set before setting Office [Math](../../) justification.

## Examples




Shows how to set office math display formatting. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Office math.docx");

auto officeMath = System::DynamicCast<OfficeMath>(doc->GetChild(NodeType::OfficeMath, 0, true));

// OfficeMath nodes that are children of other OfficeMath nodes are always inline.
// The node we are working with is the base node to change its location and display type.
ASSERT_EQ(MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// OOXML and WML formats use the "EquationXmlEncoding" property.
ASSERT_TRUE(officeMath->get_EquationXmlEncoding() == nullptr);

// Change the location and display type of the OfficeMath node.
officeMath->set_DisplayType(OfficeMathDisplayType::Display);
officeMath->set_Justification(OfficeMathJustification::Left);

doc->Save(ArtifactsDir + u"Shape.OfficeMath.docx");
```

