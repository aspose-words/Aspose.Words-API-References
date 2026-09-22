---
title: "طريقة Aspose::Words::Tables::CellFormat::get_HorizontalMerge"
linktitle: "get_HorizontalMerge"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::CellFormat::get_HorizontalMerge. تحدد كيفية دمج الخلية أفقياً مع خلايا أخرى في الصف في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.tables/cellformat/get_horizontalmerge/
---
## CellFormat::get_HorizontalMerge method


يحدد كيفية دمج الخلية أفقيًا مع خلايا أخرى في الصف.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_HorizontalMerge()
```


## أمثلة



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

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
