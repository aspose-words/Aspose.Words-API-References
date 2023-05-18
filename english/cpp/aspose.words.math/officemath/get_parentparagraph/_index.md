---
title: Aspose::Words::Math::OfficeMath::get_ParentParagraph method
linktitle: get_ParentParagraph
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Math::OfficeMath::get_ParentParagraph method. Retrieves the parent Paragraph of this node in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.math/officemath/get_parentparagraph/
---
## OfficeMath::get_ParentParagraph method


Retrieves the parent [Paragraph](../../../aspose.words/paragraph/) of this node.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Math::OfficeMath::get_ParentParagraph()
```


## Examples



Shows how to set office math display formatting. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Office math.docx");

auto officeMath = System::ExplicitCast<OfficeMath>(doc->GetChild(NodeType::OfficeMath, 0, true));

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

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
