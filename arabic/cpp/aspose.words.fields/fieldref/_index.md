---
title: "Aspose::Words::Fields::FieldRef class"
linktitle: "FieldRef"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldRef class. ينفّذ حقل REF. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 85000
url: /ar/cpp/aspose.words.fields/fieldref/
---
## FieldRef class


يُنفّذ الحقل REF. لتعلم المزيد، زر [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldRef : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                 public Aspose::Words::Fields::IMergeFieldSurrogate
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | يحصل أو يعيّن اسم الإشارة المرجعية المشار إليها. |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](./get_end/)() override | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IncludeNoteOrComment](./get_includenoteorcomment/)() | يحصل على ما إذا كان يجب زيادة أرقام الهوامش السفلية، الهوامش العليا، والتعليقات التي تم وضع علامة عليها بالإشارة المرجعية، وإدراج نص الهوامش السفلية، الهوامش العليا، والتعليق المقابل. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | يحصل على ما إذا كان يجب إنشاء ارتباط تشعبي إلى الفقرة المرجعية. |
| [get_InsertParagraphNumber](./get_insertparagraphnumber/)() | يحصل على ما إذا كان يجب إدراج رقم الفقرة للفقرة المشار إليها بالضبط كما يظهر في المستند. |
| [get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/)() | يحصل على ما إذا كان يجب إدراج رقم الفقرة للفقرة المشار إليها في السياق الكامل. |
| [get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/)() | يحصل على ما إذا كان يجب إدراج رقم الفقرة للفقرة المشار إليها في السياق النسبي. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | يحصل على ما إذا كان يجب إدراج الموقع النسبي للفقرة المشار إليها. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_NumberSeparator](./get_numberseparator/)() | يحصل على تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](./get_separator/)() override | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](./get_start/)() override | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_SuppressNonDelimiters](./get_suppressnondelimiters/)() | يحصل على ما إذا كان يجب كتم الأحرف غير الفاصلة. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FieldRef::get_BookmarkName](./get_bookmarkname/). |
| [set_IncludeNoteOrComment](./set_includenoteorcomment/)(bool) | يعيّن ما إذا كان يجب زيادة أرقام الهوامش السفلية، الهوامش العليا، والتعليقات التي تم وضع علامة عليها بالإشارة المرجعية، وإدراج نص الهوامش السفلية، الهوامش العليا، والتعليق المقابل. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | يعيّن ما إذا كان يجب إنشاء ارتباط تشعبي إلى الفقرة المرجعية. |
| [set_InsertParagraphNumber](./set_insertparagraphnumber/)(bool) | يعيّن ما إذا كان يجب إدراج رقم الفقرة للفقرة المشار إليها بالضبط كما يظهر في المستند. |
| [set_InsertParagraphNumberInFullContext](./set_insertparagraphnumberinfullcontext/)(bool) | يعيّن ما إذا كان يجب إدراج رقم الفقرة للفقرة المشار إليها في السياق الكامل. |
| [set_InsertParagraphNumberInRelativeContext](./set_insertparagraphnumberinrelativecontext/)(bool) | يضبط ما إذا كان سيتم إدراج رقم الفقرة للفقرة المشار إليها في السياق النسبي. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | يضبط ما إذا كان سيتم إدراج الموضع النسبي للفقرة المشار إليها. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberSeparator](./set_numberseparator/)(const System::String\&) | يضبط تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SuppressNonDelimiters](./set_suppressnondelimiters/)(bool) | يضبط ما إذا كان سيتم قمع الأحرف غير الفاصلة. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |

## أمثلة



يظهر كيفية إنشاء نص معلم باستخدام حقل SET، ثم عرضه في المستند باستخدام حقل REF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// سمّ النص المعلم بحقل SET.
// يشير هذا الحقل إلى "bookmark" وليس إلى بنية علامة مرجعية تظهر داخل النص، بل إلى متغيّر مسمى.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// اشر إلى العلامة المرجعية بالاسم في حقل REF واعرض محتوياتها.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
