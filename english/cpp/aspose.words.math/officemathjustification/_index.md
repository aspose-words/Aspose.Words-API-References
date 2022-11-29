---
title: OfficeMathJustification
second_title: Aspose.Words for C++ API Reference
description: Specifies the justification of the equation.
type: docs
weight: 40
url: /cpp/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enum


Specifies the justification of the equation.

```cpp
enum class OfficeMathJustification
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| CenterGroup | 1 | Justifies instances of mathematical text to the left with respect to each other, and centers the group of mathematical text (the [Math](../)[Paragraph](../../aspose.words/paragraph/)) with respect to the page. |
| Center | 2 | Centers each instance of mathematical text individually with respect to margins. |
| Left | 3 | Left justification of [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Right | 4 | Right Justification of [Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Inline | 7 | [Inline](../../aspose.words/inline/) position of [Math](../). |
| Default | n/a | Default value [CenterGroup](./). |


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

## See Also

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words](../../)
