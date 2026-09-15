---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks طريقة"
linktitle: "get_ForcePageBreaks"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks طريقة. يسمح بتحديد ما إذا كان يجب الحفاظ على فواصل الصفحات أثناء التصدير. القيمة الافتراضية هي false في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/txtsaveoptionsbase/get_forcepagebreaks/
---
## TxtSaveOptionsBase::get_ForcePageBreaks method


يسمح بتحديد ما إذا كان يجب الحفاظ على فواصل الصفحات أثناء التصدير. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks() const
```


## أمثلة



يوضح كيفية تحديد ما إذا كان يجب الحفاظ على فواصل الصفحات عند تصدير مستند إلى نص عادي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3");

// إنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى "Save" الخاص بالمستند
// طريقة لتعديل طريقة حفظ المستند إلى نص عادي.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// كائنات Aspose.Words "Document" تحتوي على فواصل صفحات، مثل مستندات Microsoft Word.
// تنسيقات الحفظ مثل ".txt" هي نص مستمر واحد بدون فواصل صفحات.
// اضبط خاصية "ForcePageBreaks" إلى "true" للحفاظ على جميع فواصل الصفحات على شكل أحرف '\\f'.
// اضبط خاصية "ForcePageBreaks" إلى "false" لتجاهل جميع فواصل الصفحات.
saveOptions->set_ForcePageBreaks(forcePageBreaks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt", saveOptions);

// إذا قمنا بتحميل مستند نص عادي يحتوي على فواصل صفحات،
// سوف يستخدم كائن "Document" هذه الفواصل لتقسيم النص إلى صفحات.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt");

ASSERT_EQ(forcePageBreaks ? 3 : 1, doc->get_PageCount());
```

## انظر أيضًا

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
