---
title: "Aspose::Words::Tables::CellMerge تعداد"
linktitle: "CellMerge"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::CellMerge تعداد. يحدد كيفية دمج خلية في جدول مع خلايا أخرى في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.tables/cellmerge/
---
## CellMerge enum


يحدد كيفية دمج خلية في جدول مع خلايا أخرى.

```cpp
enum class CellMerge
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | الخلية غير مدمجة. |
| الأول | 1 | الخلية هي الخلية الأولى في نطاق من الخلايا المدمجة. |
| السابق | 2 | يتم دمج الخلية مع الخلية السابقة أفقياً أو عمودياً. |


## أمثلة



يوضح كيفية دمج خلايا الجدول عمودياً.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدخل خلية في العمود الأول من الصف الأول.
// ستكون هذه الخلية الأولى في مجموعة من الخلايا المدمجة عمودياً.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// أدخل خلية في العمود الثاني من الصف الأول، ثم أنهِ الصف.
// أيضاً، قم بضبط المُنشئ لتعطيل الدمج العمودي في الخلايا التي تم إنشاؤها.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// أدخل خلية في العمود الأول من الصف الثاني.
// بدلاً من إضافة محتوى نصي، سندمج هذه الخلية مع الخلية الأولى التي أضفناها مباشرةً أعلاه.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// أدخل خلية مستقلة أخرى في العمود الثاني من الصف الثاني.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```


يوضح كيفية دمج خلايا الجدول أفقياً.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدخل خلية في العمود الأول من الصف الأول.
// ستكون هذه الخلية الأولى في مجموعة من الخلايا المدمجة أفقياً.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// أدخل خلية في العمود الثاني من الصف الأول. بدلاً من إضافة محتوى نصي،
// سندمج هذه الخلية مع الخلية الأولى التي أضفناها مباشرةً إلى اليسار.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::Previous);
builder->EndRow();

// أدخل خليتين إضافيتين غير مدمجتين إلى الصف الثاني.
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.HorizontalMerge.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
