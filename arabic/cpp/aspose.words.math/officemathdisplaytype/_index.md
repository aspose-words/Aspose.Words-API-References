---
title: "Aspose::Words::Math::OfficeMathDisplayType enum"
linktitle: "OfficeMathDisplayType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Math::OfficeMathDisplayType enum. يحدد نوع تنسيق العرض للمعادلة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enum


يحدد نوع تنسيق العرض للمعادلة.

```cpp
enum class OfficeMathDisplayType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Display | 0 | يتم عرض Office [Math](../) على سطر منفصل. |
| Inline | 1 | يتم عرض Office [Math](../) مضمنًا مع النص. |


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

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
