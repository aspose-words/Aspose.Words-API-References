---
title: "الفئة Aspose::Words::Fields::FieldMacroButton"
linktitle: "FieldMacroButton"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "الفئة Aspose::Words::Fields::FieldMacroButton. تنفّذ حقل MACROBUTTON. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 65000
url: /ar/cpp/aspose.words.fields/fieldmacrobutton/
---
## FieldMacroButton class


ينفذ حقل MACROBUTTON. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMacroButton : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IMergeFieldSurrogate
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_DisplayText](./get_displaytext/)() | يحصل أو يضبط النص الذي سيظهر كـ "زر" يتم اختياره لتشغيل الماكرو أو الأمر. |
| [get_End](./get_end/)() override | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_MacroName](./get_macroname/)() | يحصل أو يضبط اسم الماكرو أو الأمر لتشغيله. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](./get_separator/)() override | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](./get_start/)() override | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_DisplayText](./set_displaytext/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FieldMacroButton::get_DisplayText](./get_displaytext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_MacroName](./set_macroname/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FieldMacroButton::get_MacroName](./get_macroname/). |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
## ملاحظات


يسمح بتشغيل ماكرو أو أمر.

في Aspose.Words يمكن لهذا الحقل أيضًا أن يعمل كحقل دمج.

## أمثلة



يوضح كيفية استخدام حقول MACROBUTTON للسماح لنا بتشغيل ماكروات المستند بالنقر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// أدرج حقل MACROBUTTON، واشر إلى أحد ماكروات المستند بالاسم في خاصية MacroName.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(System::String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// استخدم الخاصية للإشارة إلى "ViewZoom200"، ماكرو يأتي مع Microsoft Word.
// يمكننا العثور على جميع الماكرو الأخرى عبر View -> Macros (القائمة المنسدلة) -> View Macros.
// في ذلك القائمة، اختر "Word Commands" من القائمة المنسدلة "Macros in:".
// إذا كان المستند يحتوي على ماكرو مخصص يحمل نفس اسم ماكرو أساسي،
// سيكون ماكرو الخاص بنا هو الذي يتم تشغيله بواسطة حقل MACROBUTTON.
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(System::String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// احفظ المستند كنوع مستند يدعم الماكرو.
doc->Save(get_ArtifactsDir() + u"Field.MACROBUTTON.docm");
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
