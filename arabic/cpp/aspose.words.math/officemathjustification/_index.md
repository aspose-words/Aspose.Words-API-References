---
title: "Aspose::Words::Math::OfficeMathJustification enum"
linktitle: "OfficeMathJustification"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Math::OfficeMathJustification enum. يحدد محاذاة المعادلة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enum


يحدد محاذاة المعادلة.

```cpp
enum class OfficeMathJustification
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| CenterGroup | 1 | يضبط محاذاة حالات النص الرياضي إلى اليسار بالنسبة لبعضها البعض، ويُوسّط مجموعة النص الرياضي (الـ[Math](../)[Paragraph](../../aspose.words/paragraph/)) بالنسبة للصفحة. |
| وسط | 2 | يُوسّط كل حالة من النص الرياضي بشكل فردي بالنسبة للهوامش. |
| Left | 3 | محاذاة إلى اليسار للـ[Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Right | 4 | محاذاة إلى اليمين للـ[Math](../)[Paragraph](../../aspose.words/paragraph/). |
| Inline | 7 | موضع [Inline](../../aspose.words/inline/) للـ[Math](../). |
| Default | n/a | القيمة الافتراضية لـ[CenterGroup](./). |


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
