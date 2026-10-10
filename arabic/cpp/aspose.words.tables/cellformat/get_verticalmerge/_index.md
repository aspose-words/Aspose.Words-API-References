---
title: "Aspose::Words::Tables::CellFormat::get_VerticalMerge طريقة"
linktitle: "get_VerticalMerge"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::CellFormat::get_VerticalMerge طريقة. يحدد كيفية دمج الخلية مع خلايا أخرى عموديًا في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.tables/cellformat/get_verticalmerge/
---
## CellFormat::get_VerticalMerge method


يحدد كيفية دمج الخلية مع خلايا أخرى عموديًا.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_VerticalMerge()
```

## ملاحظات


يمكن دمج الخلايا عموديًا فقط إذا كانت حدودها اليسرى واليمنى متطابقة.

عند دمج الخلايا عموديًا، يتم توحيد مناطق العرض للخلايا المدمجة. تُستخدم المنطقة الموحدة لعرض محتويات الخلية المدمجة أولاً ويجب أن تكون جميع الخلايا المدمجة عموديًا الأخرى فارغة.

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

## انظر أيضًا

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
