---
title: "طريقة Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout"
linktitle: "get_PreserveTableLayout"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout. تحدد ما إذا كان البرنامج يجب أن يحاول الحفاظ على تخطيط الجداول عند الحفظ بصيغة النص العادي. القيمة الافتراضية هي false في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/txtsaveoptions/get_preservetablelayout/
---
## TxtSaveOptions::get_PreserveTableLayout method


يحدد ما إذا كان البرنامج يجب أن يحاول الحفاظ على تخطيط الجداول عند الحفظ بتنسيق النص العادي. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_PreserveTableLayout() const
```


## أمثلة



يوضح كيفية الحفاظ على تخطيط الجداول عند التحويل إلى نص عادي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1");
builder->InsertCell();
builder->Write(u"Row 2, cell 2");
builder->EndTable();

// إنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل طريقة حفظ المستند كنص عادي.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// عيّن الخاصية "PreserveTableLayout" إلى "true" لتطبيق حشو فراغات على المحتوى
// في مستند النص العادي الناتج للحفاظ على أكبر قدر ممكن من تخطيط الجدول.
// عيّن الخاصية "PreserveTableLayout" إلى "false" لحفظ محتويات جميع الجداول
// كجسم نصي مستمر، مع سطر جديد فقط لكل صف.
txtSaveOptions->set_PreserveTableLayout(preserveTableLayout);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
{
    ASSERT_EQ(System::String(u"Row 1, cell 1                                            Row 1, cell 2\r\n") + u"Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
}
else
{
    ASSERT_EQ(System::String(u"Row 1, cell 1\r") + u"Row 1, cell 2\r" + u"Row 2, cell 1\r" + u"Row 2, cell 2\r\r\n", docText);
}
```

## انظر أيضًا

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
