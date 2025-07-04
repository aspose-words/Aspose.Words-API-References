---
title: Aspose::Words::Math::OfficeMath::get_DisplayType method
linktitle: get_DisplayType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Math::OfficeMath::get_DisplayType method. Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text or displayed on its own line in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.math/officemath/get_displaytype/
---
## OfficeMath::get_DisplayType method


Gets/sets Office [Math](../../) display format type which represents whether an equation is displayed inline with the text or displayed on its own line.

```cpp
Aspose::Words::Math::OfficeMathDisplayType Aspose::Words::Math::OfficeMath::get_DisplayType()
```

## Remarks


Display format type has effect for top level Office [Math](../../) only.

Returned display format type is always [Inline](../../officemathdisplaytype/) for nested Office [Math](../../).

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

* Enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
