---
title: "Aspose::Words::Notes::FootnoteOptions::get_Columns طريقة"
linktitle: "get_Columns"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Notes::FootnoteOptions::get_Columns طريقة. يحدد عدد الأعمدة التي يتم تنسيق منطقة الحواشي بها في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.notes/footnoteoptions/get_columns/
---
## FootnoteOptions::get_Columns method


يحدد عدد الأعمدة التي يتم تنسيق منطقة الحواشي السفلية بها.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_Columns()
```


## أمثلة



يظهر كيفية تقسيم قسم الحواشي السفلية إلى عدد محدد من الأعمدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```

## انظر أيضًا

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
