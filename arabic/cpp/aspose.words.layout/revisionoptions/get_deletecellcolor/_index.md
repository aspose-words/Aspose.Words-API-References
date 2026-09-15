---
title: "طريقة Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor"
linktitle: "get_DeleteCellColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor method. تسمح بتحديد اللون الذي سيُستخدم للخلايا المحذوفة Deletion. القيمة الافتراضية هي Pink في C++."
type: docs
weight: 2500
url: /ar/cpp/aspose.words.layout/revisionoptions/get_deletecellcolor/
---
## RevisionOptions::get_DeleteCellColor method


تسمح بتحديد اللون الذي سيُستخدم للخلايا المحذوفة [Deletion](../../../aspose.words/revisiontype/). القيمة الافتراضية هي [Pink](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor()
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
