---
title: "Aspose::Words::Layout::RevisionOptions::get_InsertCellColor طريقة"
linktitle: "get_InsertCellColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::RevisionOptions::get_InsertCellColor طريقة. يسمح بتحديد اللون المستخدم للخلايا المُدخلة Insertion. القيمة الافتراضية هي Blue في C++."
type: docs
weight: 4500
url: /ar/cpp/aspose.words.layout/revisionoptions/get_insertcellcolor/
---
## RevisionOptions::get_InsertCellColor method


يسمح بتحديد اللون المستخدم للخلايا المُدخلة [Insertion](../../../aspose.words/revisiontype/). القيمة الافتراضية هي [Blue](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertCellColor()
```


## أمثلة



يعرض كيفية العمل مع لون مراجعة إدراج/حذف الخلية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Cell revisions.docx");

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(Aspose::Words::Layout::RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(Aspose::Words::Layout::RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```

## انظر أيضًا

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
