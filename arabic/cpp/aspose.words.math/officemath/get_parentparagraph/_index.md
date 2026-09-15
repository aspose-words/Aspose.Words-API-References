---
title: "طريقة Aspose::Words::Math::OfficeMath::get_ParentParagraph"
linktitle: "get_ParentParagraph"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Math::OfficeMath::get_ParentParagraph. تسترجع الفقرة الأصلية لهذه العقدة في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.math/officemath/get_parentparagraph/
---
## OfficeMath::get_ParentParagraph method


تسترجع الفقرة الأصلية [Paragraph](../../../aspose.words/paragraph/) لهذه العقدة.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Math::OfficeMath::get_ParentParagraph()
```


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

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
