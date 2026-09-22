---
title: "Aspose::Words::HeightRule enum"
linktitle: "HeightRule"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::HeightRule enum. يحدد القاعدة لتحديد ارتفاع كائن في C++."
type: docs
weight: 91000
url: /ar/cpp/aspose.words/heightrule/
---
## HeightRule enum


يحدد القاعدة لتحديد ارتفاع الكائن.

```cpp
enum class HeightRule
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| AtLeast | 0 | سيكون الارتفاع على الأقل هو الارتفاع المحدد بالنقاط. سيتوسع إذا لزم الأمر لاستيعاب جميع النص داخل الكائن. |
| Exactly | 1 | يتم تحديد الارتفاع بدقة بالنقاط. يرجى ملاحظة أنه إذا لم يتمكن النص من الملاءمة داخل الكائن بهذا الارتفاع، فسيظهر مقطوعًا. |
| تلقائي | 2 | سيزداد الارتفاع تلقائيًا لاستيعاب جميع النص داخل الكائن. |


## أمثلة



يوضح كيفية تنسيق الصفوف باستخدام منشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// ابدأ صفًا ثانيًا، ثم قم بتكوين ارتفاعه. سيطبق المنشئ هذه الإعدادات على
// صفه الحالي، وكذلك أي صفوف جديدة ينشئها لاحقًا.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// لم يتأثر الصف الأول بإعادة تكوين الحشو ولا يزال يحتفظ بالقيم الافتراضية.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
