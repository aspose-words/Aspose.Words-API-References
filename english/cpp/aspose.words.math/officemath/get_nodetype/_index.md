---
title: Aspose::Words::Math::OfficeMath::get_NodeType method
linktitle: get_NodeType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Math::OfficeMath::get_NodeType method. Returns OfficeMath in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.math/officemath/get_nodetype/
---
## OfficeMath::get_NodeType method


Returns [OfficeMath](../../../aspose.words/nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::Math::OfficeMath::get_NodeType() const override
```


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

// Change the location and display type of the OfficeMath node.
officeMath->set_DisplayType(OfficeMathDisplayType::Display);
officeMath->set_Justification(OfficeMathJustification::Left);

doc->Save(ArtifactsDir + u"Shape.OfficeMath.docx");
```

## See Also

* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
