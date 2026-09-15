---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks طريقة"
linktitle: "get_ShowParagraphMarks"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks طريقة. يحصل أو يضبط إشارة إلى ما إذا كانت علامات الفقرات تُعرض. القيمة الافتراضية هي false في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.layout/layoutoptions/get_showparagraphmarks/
---
## LayoutOptions::get_ShowParagraphMarks method


يحصل أو يعيّن إشارة ما إذا كانت علامات الفقرات تُعرض. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks() const
```


## أمثلة



يظهر كيفية إظهار علامات الفقرات في مستند الإخراج المرسوم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف بعض الفقرات، ثم فعّل علامات الفقرات لإظهار نهايات الفقرات
// مع رمز الفقرة (¶) عند رسم المستند.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```

## انظر أيضًا

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
