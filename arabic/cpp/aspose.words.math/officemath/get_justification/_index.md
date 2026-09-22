---
title: "طريقة Aspose::Words::Math::OfficeMath::get_Justification"
linktitle: "get_Justification"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Math::OfficeMath::get_Justification. يحصل/يضبط مبرر Office Math في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.math/officemath/get_justification/
---
## OfficeMath::get_Justification method


يحصل/يضبط مبرر Office [Math](../../).

```cpp
Aspose::Words::Math::OfficeMathJustification Aspose::Words::Math::OfficeMath::get_Justification()
```

## ملاحظات


لا يمكن ضبط المبرر لـ Office [Math](../../) بنوع تنسيق العرض [Inline](../../officemathdisplaytype/).

[Inline](../../../aspose.words/inline/) justification cannot be set to the Office [Math](../../) with display format type [Display](../../officemathdisplaytype/).

يجب ضبط [DisplayType](../get_displaytype/) المقابل قبل ضبط مبرر Office [Math](../../).

## أمثلة



يظهر كيفية ضبط تنسيق عرض Office Math.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto officeMath = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// عُقَد OfficeMath التي هي أبناء لعُقَد OfficeMath أخرى تكون دائمًا inline.
// العقدة التي نعمل معها هي العقدة الأساسية لتغيير موقعها ونوع العرض.
ASSERT_EQ(Aspose::Words::Math::MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(Aspose::Words::NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// غيّر موقع ونوع عرض عقدة OfficeMath.
officeMath->set_DisplayType(Aspose::Words::Math::OfficeMathDisplayType::Display);
officeMath->set_Justification(Aspose::Words::Math::OfficeMathJustification::Left);

doc->Save(get_ArtifactsDir() + u"Shape.OfficeMath.docx");
```

## انظر أيضًا

* Enum [OfficeMathJustification](../../officemathjustification/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
