---
title: "فئة Aspose::Words::Fields::FieldChar"
linktitle: "FieldChar"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldChar. الفئة الأساسية للعُقد التي تمثل أحرف الحقل في مستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words.fields/fieldchar/
---
## FieldChar class


الفئة الأساسية للعُقَد التي تمثل أحرف الحقل في المستند. لمزيد من المعلومات، زر [العمل مع الحقول](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldChar : public Aspose::Words::SpecialChar
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](../../aspose.words/specialchar/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [Clone](../../aspose.words/node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_FieldType](./get_fieldtype/)() const | يعيد نوع الحقل. |
| [get_Font](../../aspose.words/inline/get_font/)() | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | يعيد **true** إذا كان بإمكان هذه العقدة احتواء عقد أخرى. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | يرجع true إذا تم حذف هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsDirty](./get_isdirty/)() const | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | يرجع true إذا تم تغيير تنسيق الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | يرجع true إذا تم إدراج هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsLocked](./get_islocked/)() const | يحصل أو يعيّن ما إذا كان الحقل الأب مقفلاً (يجب عدم إعادة حساب نتيجته). |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | يرجع **true** إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | يرجع **true** إذا تم نقل (إدراج) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](../../aspose.words/specialchar/get_nodetype/)() const override | يعيد [SpecialChar](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | يسترجع الفقرة الأب [Paragraph](../../aspose.words/paragraph/) لهذه العقدة. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | يرجع كائن [Range](../../aspose.words/range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](./getfield/)() | يعيد حقلًا لحرف الحقل. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | يحصل على الحرف الخاص الذي تمثله هذه العقدة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من العنصر الأب. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsDirty](./set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FieldChar::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FieldChar::get_IsLocked](./get_islocked/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


الحقل الكامل في مستند Microsoft Word هو بنية معقدة تتكوّن من حرف بدء الحقل، رمز الحقل، حرف فاصل الحقل، نتيجة الحقل وحرف نهاية الحقل. بعض الحقول تحتوي فقط على بدء الحقل، رمز الحقل ونهاية الحقل.

لإدراج حقل جديد بسهولة في مستند، استخدم طريقة [InsertField()](../).

## أمثلة



يظهر كيفية العمل مع عقدة [FieldStart](../fieldstart/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->get_Format()->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

System::SharedPtr<Aspose::Words::Fields::FieldChar> fieldStart = field->get_Start();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, fieldStart->get_FieldType());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsDirty());
ASPOSE_ASSERT_EQ(false, fieldStart->get_IsLocked());

// استرجع كائن الواجهة الذي يمثل الحقل في المستند.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(fieldStart->GetField());

ASPOSE_ASSERT_EQ(false, field->get_IsLocked());
ASSERT_EQ(u" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// حدّث الحقل لعرض التاريخ الحالي.
field->Update();
```

## انظر أيضًا

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
