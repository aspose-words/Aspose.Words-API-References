---
title: "طريقة Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars"
linktitle: "get_ShowRevisionBars"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars. يسمح بتحديد ما إذا كان يجب عرض أشرطة المراجعة بالقرب من الأسطر التي تحتوي على محتوى مُعدَّل. القيمة الافتراضية هي true في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.layout/revisionoptions/get_showrevisionbars/
---
## RevisionOptions::get_ShowRevisionBars method


يسمح بتحديد ما إذا كان يجب عرض أشرطة المراجعة بالقرب من السطور التي تحتوي على محتوى مُراجع. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars() const
```


## أمثلة



يظهر كيفية تعديل مظهر المراجعات في مستند الإخراج المرسوم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج مراجعة، ثم غيّر لون جميع المراجعات إلى الأخضر.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// أزل الشريط الذي يظهر إلى يسار كل سطر مُراجَع.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## انظر أيضًا

* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
