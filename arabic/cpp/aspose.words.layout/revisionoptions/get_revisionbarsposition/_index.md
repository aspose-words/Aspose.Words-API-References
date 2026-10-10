---
title: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition طريقة"
linktitle: "get_RevisionBarsPosition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition طريقة. يحصل أو يضبط موضع عرض أشرطة المراجعة. القيمة الافتراضية هي Outside في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.layout/revisionoptions/get_revisionbarsposition/
---
## RevisionOptions::get_RevisionBarsPosition method


يحصل أو يضبط موضع عرض أشرطة المراجعة. القيمة الافتراضية هي [Outside](../../../aspose.words.drawing/horizontalalignment/).

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition() const
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

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
