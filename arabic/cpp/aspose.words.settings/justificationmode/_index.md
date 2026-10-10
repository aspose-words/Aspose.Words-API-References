---
title: "Aspose::Words::Settings::JustificationMode enum"
linktitle: "JustificationMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Settings::JustificationMode enum. يحدد تعديل تباعد الأحرف لمستند. القيمة الافتراضية هي Expand في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.settings/justificationmode/
---
## JustificationMode enum


يحدد تعديل تباعد الأحرف للمستند. القيمة الافتراضية هي **Expand**.

```cpp
enum class JustificationMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Expand | 0 | لا تقم بضغط تباعد الأحرف. |
| Compress | 1 | ضغط تباعد الأحرف. |
| CompressKana | 2 | ضغط، باستخدام قواعد مقاطع الكانا، هيراغانا وكاتاكانا. |


## أمثلة



يوضح كيفية إدارة التحكم في تباعد الأحرف.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
