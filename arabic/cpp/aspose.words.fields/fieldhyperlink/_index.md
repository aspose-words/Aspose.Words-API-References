---
title: "فئة Aspose::Words::Fields::FieldHyperlink"
linktitle: "FieldHyperlink"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldHyperlink. تنفّذ حقل HYPERLINK. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 53000
url: /ar/cpp/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class


يطبق حقل HYPERLINK. لمعرفة المزيد، قم بزيارة [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldHyperlink : public Aspose::Words::Fields::Field,
                       public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                       public Aspose::Words::Fields::IFieldResultFormatProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Address](./get_address/)() | يحصل أو يعيّن موقعًا يقفز إليه هذا الارتباط التشعبي. |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsImageMap](./get_isimagemap/)() | يحصل أو يعيّن ما إذا كان سيتم إلحاق إحداثيات بالارتباط التشعبي لخريطة صورة من جانب الخادم. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_OpenInNewWindow](./get_openinnewwindow/)() | يحصل أو يعيّن ما إذا كان سيتم فتح الموقع الوجهة في نافذة متصفح ويب جديدة. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_ScreenTip](./get_screentip/)() | يحصل أو يعيّن نص تلميح الشاشة للارتباط التشعبي. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_SubAddress](./get_subaddress/)() | يحصل أو يعيّن موقعًا في الملف، مثل إشارة مرجعية، يقفز إليه هذا الارتباط التشعبي. |
| [get_Target](./get_target/)() | يحصل أو يعيّن الهدف الذي يجب إعادة توجيه الرابط إليه. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_Address](./set_address/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldHyperlink::get_Address](./get_address/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsImageMap](./set_isimagemap/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FieldHyperlink::get_IsImageMap](./get_isimagemap/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_OpenInNewWindow](./set_openinnewwindow/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow](./get_openinnewwindow/). |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScreenTip](./set_screentip/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldHyperlink::get_ScreenTip](./get_screentip/). |
| [set_SubAddress](./set_subaddress/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldHyperlink::get_SubAddress](./get_subaddress/). |
| [set_Target](./set_target/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldHyperlink::get_Target](./get_target/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |

## أمثلة



يعرض كيفية استخدام حقول HYPERLINK للربط بالمستندات في نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// عند النقر على حقل HYPERLINK هذا في Microsoft Word،
// سيفتح المستند المرتبط ثم يضع المؤشر عند الإشارة المرجعية المحددة.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// عند النقر على حقل HYPERLINK هذا في Microsoft Word،
// سيفتح المستند المرتبط، ويقوم بالتمرير تلقائيًا إلى الإطار المضمن المحدد.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
