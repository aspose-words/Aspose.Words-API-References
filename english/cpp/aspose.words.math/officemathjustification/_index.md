---
title: Aspose::Words::Math::OfficeMathJustification enum
linktitle: OfficeMathJustification
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Math::OfficeMathJustification enum. Specifies the justification of the equation in C++.'
type: docs
weight: 4000
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
