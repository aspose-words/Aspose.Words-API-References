---
title: "طريقة Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages"
linktitle: "get_AllowBreakAcrossPages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages. صحيحة إذا كان مسموحًا للنص في صف الجدول أن ينقسم عبر فاصل صفحة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.tables/rowformat/get_allowbreakacrosspages/
---
## RowFormat::get_AllowBreakAcrossPages method


صحيح إذا كان مسموحًا للنص في صف الجدول أن ينقسم عبر فاصل صفحة.

```cpp
bool Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages()
```


## أمثلة



يعرض كيفية تعطيل انقسام الصفوف عبر الصفحات لكل صف في جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// قم بتعيين خاصية "AllowBreakAcrossPages" إلى "false" للحفاظ على الصف
// ككامل واحد إذا امتد الجدول على صفحتين، مما يؤدي إلى انقسامه على طول ذلك الصف.
// إذا كان الصف كبيرًا جدًا بحيث لا يتسع في صفحة واحدة، سيقوم Microsoft Word بنقله إلى الصفحة التالية.
// قم بتعيين خاصية "AllowBreakAcrossPages" إلى "true" للسماح للصف بالانقسام عبر صفحتين.
for (auto&& row : System::IterateOver<Aspose::Words::Tables::Row>(table))
{
    row->get_RowFormat()->set_AllowBreakAcrossPages(allowBreakAcrossPages);
}

doc->Save(get_ArtifactsDir() + u"Table.AllowBreakAcrossPages.docx");
```

## انظر أيضًا

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
