---
title: "Aspose::Words::Range::NormalizeFieldTypes method"
linktitle: "NormalizeFieldTypes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Range::NormalizeFieldTypes طريقة. يغيّر قيم نوع الحقل FieldType لـ FieldStart و FieldSeparator و FieldEnd في هذا النطاق بحيث تتطابق مع أنواع الحقول الموجودة في أكواد الحقول في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words/range/normalizefieldtypes/
---
## Range::NormalizeFieldTypes method


يغيّر قيم نوع الحقل [FieldType](../../../aspose.words.fields/fieldchar/get_fieldtype/) لـ [FieldStart](../../../aspose.words.fields/fieldstart/)، [FieldSeparator](../../../aspose.words.fields/fieldseparator/)، [FieldEnd](../../../aspose.words.fields/fieldend/) في هذا النطاق بحيث تتطابق مع أنواع الحقول الموجودة في أكواد الحقول.

```cpp
void Aspose::Words::Range::NormalizeFieldTypes()
```

## ملاحظات


استخدم هذه الطريقة بعد تغييرات المستند التي تؤثر على أنواع الحقول.

لتغيير قيم نوع الحقل في المستند بأكمله استخدم [NormalizeFieldTypes](../../document/normalizefieldtypes/).

## أمثلة



يوضح كيفية الحفاظ على تحديث نوع الحقل مع كود الحقل الخاص به.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE", nullptr);

// تكتشف Aspose.Words أنواع الحقول تلقائيًا بناءً على أكواد الحقول.
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());

// قم بتغيير النص الخام للحقل يدويًا، والذي يحدد كود الحقل.
auto fieldText = System::ExplicitCast<Aspose::Words::Run>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(0));
fieldText->set_Text(u"PAGE");

// تغيير كود الحقل قد حول هذا الحقل إلى نوع مختلف،
// لكن خصائص نوع الحقل لا تزال تعرض النوع القديم.
ASSERT_EQ(u"PAGE", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_End()->get_FieldType());

// حدّث تلك الخصائص باستخدام هذه الطريقة لعرض القيمة الحالية.
doc->NormalizeFieldTypes();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_End()->get_FieldType());
```

## انظر أيضًا

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
