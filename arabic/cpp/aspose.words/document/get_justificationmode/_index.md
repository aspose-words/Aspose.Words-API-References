---
title: "طريقة Aspose::Words::Document::get_JustificationMode"
linktitle: "get_JustificationMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_JustificationMode. يحصل أو يضبط تعديل تباعد الأحرف للمستند في C++."
type: docs
weight: 34000
url: /ar/cpp/aspose.words/document/get_justificationmode/
---
## Document::get_JustificationMode method


يحصل أو يضبط تعديل تباعد الأحرف في المستند.

```cpp
Aspose::Words::Settings::JustificationMode Aspose::Words::Document::get_JustificationMode()
```


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

* Enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
