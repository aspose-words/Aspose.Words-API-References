---
title: "فئة Aspose::Words::Fields::FieldUserInitials"
linktitle: "FieldUserInitials"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldUserInitials. تنفذ حقل USERINITIALS. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 109000
url: /ar/cpp/aspose.words.fields/fielduserinitials/
---
## FieldUserInitials class


ينفّذ حقل USERINITIALS. لمعرفة المزيد، زر مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldUserInitials : public Aspose::Words::Fields::Field
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [get_UserInitials](./get_userinitials/)() | يحصل أو يضبط الأحرف الأولى للمستخدم الحالي. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_UserInitials](./set_userinitials/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FieldUserInitials::get_UserInitials](./get_userinitials/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |

## أمثلة



يوضح كيفية استخدام حقل USERINITIALS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أنشئ كائن UserInformation وضعه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// أنشئ حقل USERINITIALS لعرض الأحرف الأولى للمستخدم الحالي،
// مستمد من كائن UserInformation الذي أنشأناه أعلاه.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<Aspose::Words::Fields::FieldUserInitials>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// يمكننا تعيين هذه الخاصية لجعل حقلنا يتجاوز القيمة المخزنة حاليًا في كائن UserInformation.
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// هذا لا يؤثر على القيمة في كائن UserInformation.
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERINITIALS.docx");
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
