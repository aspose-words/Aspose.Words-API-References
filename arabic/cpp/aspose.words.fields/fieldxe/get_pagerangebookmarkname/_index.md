---
title: "Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName طريقة"
linktitle: "get_PageRangeBookmarkName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName طريقة. يحصل أو يضبط اسم العلامة المرجعية التي تحدد نطاق الصفحات والذي يتم إدراجه كرقم صفحة الإدخال في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.fields/fieldxe/get_pagerangebookmarkname/
---
## FieldXE::get_PageRangeBookmarkName method


يحصل أو يضبط اسم الإشارة المرجعية التي تحدد نطاق صفحات يتم إدراجه كرقم صفحة الإدخال.

```cpp
System::String Aspose::Words::Fields::FieldXE::get_PageRangeBookmarkName()
```


## أمثلة



يظهر كيفية تحديد الصفحات التي يغطيها العلامة المرجعية كنطاق صفحات لإدخال حقل INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء حقل INDEX سيعرض مدخلاً لكل حقل XE يُعثر عليه في المستند.
// سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
// سيجمع إدخال INDEX جميع حقول XE ذات القيم المطابقة في خاصية "Text".
// في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// بالنسبة لإدخالات INDEX التي تعرض نطاقات صفحات، يمكننا تحديد سلسلة فاصل
// ستظهر بين رقم الصفحة الأولى ورقم الصفحة الأخيرة.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageRangeSeparator(u" to ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\g \" to \"", index->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"My entry");

// إذا كان حقل XE يحدد علامة مرجعية باستخدام خاصية PageRangeBookmarkName،
// سوف يظهر إدخال INDEX نطاق الصفحات التي تغطيها العلامة المرجعية
// بدلاً من رقم الصفحة التي تحتوي على حقل XE.
indexEntry->set_PageRangeBookmarkName(u"MyBookmark");

ASSERT_EQ(u" XE  \"My entry\" \\r MyBookmark", indexEntry->GetFieldCode());
ASSERT_EQ(u"MyBookmark", indexEntry->get_PageRangeBookmarkName());

// أدرج علامة مرجعية تبدأ في الصفحة 3 وتنتهي في الصفحة 5.
// سوف يعرض إدخال INDEX لحقل XE الذي يشير إلى هذه العلامة المرجعية هذا النطاق الصفحي.
// في جدولنا، سيعرض إدخال INDEX النص "إدخالي، على الصفحات 3 إلى 5".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Start of MyBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"End of MyBookmark");
builder->EndBookmark(u"MyBookmark");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageRangeBookmark.docx");
```

## انظر أيضًا

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
