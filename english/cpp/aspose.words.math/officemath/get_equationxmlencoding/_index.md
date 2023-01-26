---
title: get_EquationXmlEncoding
second_title: Aspose.Words for C++ API Reference
description: Gets/sets an encoding that was used to encode equation XML, if this office math object is read from equation XML.
type: docs
weight: 40
url: /cpp/aspose.words.math/officemath/get_equationxmlencoding/
---
## OfficeMath::get_EquationXmlEncoding method


Gets/sets an encoding that was used to encode equation XML, if this office math object is read from equation XML.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Math::OfficeMath::get_EquationXmlEncoding()
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

// OOXML and WML formats use the "EquationXmlEncoding" property.
ASSERT_TRUE(officeMath->get_EquationXmlEncoding() == nullptr);

// Change the location and display type of the OfficeMath node.
officeMath->set_DisplayType(OfficeMathDisplayType::Display);
officeMath->set_Justification(OfficeMathJustification::Left);

doc->Save(ArtifactsDir + u"Shape.OfficeMath.docx");
```

## See Also

* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words](../../../)
