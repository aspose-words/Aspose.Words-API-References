---
title: "طريقة Aspose::Words::Fields::ToaCategories::idx_set"
linktitle: "idx_set"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::ToaCategories::idx_set. يحصل أو يعيّن عنوان الفئة حسب رقم الفئة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.fields/toacategories/idx_set/
---
## ToaCategories::idx_set method


يحصل أو يعيّن عنوان الفئة حسب رقم الفئة.

```cpp
void Aspose::Words::Fields::ToaCategories::idx_set(int32_t number, const System::String &value)
```


## أمثلة



يوضح كيفية تحديد مجموعة من الفئات لحقول TOA.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حقول TOA يمكنها تصفية مدخلاتها حسب الفئات المعرفة في هذه المجموعة.
auto toaCategories = System::MakeObject<Aspose::Words::Fields::ToaCategories>();
doc->get_FieldOptions()->set_ToaCategories(toaCategories);

// تأتي هذه المجموعة من الفئات بقيم افتراضية، يمكننا استبدالها بقيم مخصصة.
ASSERT_EQ(u"Cases", toaCategories->idx_get(1));
ASSERT_EQ(u"Statutes", toaCategories->idx_get(2));

toaCategories->idx_set(1, u"My Category 1");
toaCategories->idx_set(2, u"My Category 2");

// يمكننا دائمًا الوصول إلى القيم الافتراضية عبر هذه المجموعة.
ASSERT_EQ(u"Cases", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(1));
ASSERT_EQ(u"Statutes", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(2));

// أدرج حقلي TOA. حقول TOA تنشئ مدخلًا لكل حقل TA في المستند.
// استخدم المفتاح "\c" لاختيار فهرس فئة من مجموعتنا.
//  باستخدام هذا المفتاح، سيختار حقل TOA فقط المدخلات من حقول TA التي
// تملك أيضًا مفتاح "\c" بفهرس فئة مطابق. كل حقل TOA سيعرض أيضًا
// اسم الفئة التي يشير إليها مفتاح "\c" الخاص به.
builder->InsertField(u"TOA \\c 1 \\h", nullptr);
builder->InsertField(u"TOA \\c 2 \\h", nullptr);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// أدرج مدخلات TOA عبر فئتين. سيستقبل حقل TOA الأول مدخلًا واحدًا،
// من حقل TA الثاني الذي يشير مفتاح "\c" الخاص به أيضًا إلى الفئة الأولى.
// حقل TOA الثاني سيحتوي على مدخلين من حقلي TA الآخرين.
builder->InsertField(u"TA \\c 2 \\l \"entry 1\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 1 \\l \"entry 2\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 2 \\l \"entry 3\"");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.TOA.Categories.docx");
```

## انظر أيضًا

* Class [ToaCategories](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
