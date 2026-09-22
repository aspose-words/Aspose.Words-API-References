---
title: "Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor طريقة"
linktitle: "get_InsertedTextColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor طريقة. يسمح بتحديد اللون المستخدم للمحتوى المُدرج Insertion. القيمة الافتراضية هي ByAuthor في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.layout/revisionoptions/get_insertedtextcolor/
---
## RevisionOptions::get_InsertedTextColor method


يسمح بتحديد اللون المستخدم للمحتوى المُدرج [Insertion](../../../aspose.words/revisiontype/). القيمة الافتراضية هي [ByAuthor](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor()
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

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
