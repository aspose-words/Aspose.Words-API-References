---
title: "Aspose::Words::Fields::FormField class"
linktitle: "FormField"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FormField class. يمثل حقل نموذج واحد. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 112000
url: /ar/cpp/aspose.words.fields/formfield/
---
## FormField class


يمثل حقل نموذج واحد. لمعرفة المزيد، زر مقالة الوثائق [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormField : public Aspose::Words::SpecialChar
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | يقبل زائرًا. |
| [Clone](../../aspose.words/node/clone/)(bool) | ينشئ نسخة مكررة من العقدة. |
| [get_CalculateOnExit](./get_calculateonexit/)() | صحيح إذا تم تحديث الإشارات إلى حقل النموذج المحدد تلقائيًا كلما تم الخروج من الحقل. |
| [get_CheckBoxSize](./get_checkboxsize/)() | يحصل أو يعيّن حجم خانة الاختيار بالنقاط. لا يكون له تأثير إلا عندما يكون [IsCheckBoxExactSize](./get_ischeckboxexactsize/) **true**. |
| [get_Checked](./get_checked/)() | يحصل أو يعيّن حالة التحديد لحقل نموذج خانة الاختيار. القيمة الافتراضية لهذه الخاصية هي **false**. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | يحدد معرفًا مخصصًا للعقدة. |
| [get_Default](./get_default/)() | يحصل أو يعيّن القيمة الافتراضية لحقل نموذج خانة الاختيار. القيمة الافتراضية لهذه الخاصية هي **false**. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [get_DropDownItems](./get_dropdownitems/)() | يوفر الوصول إلى عناصر حقل النموذج المنسدل. |
| [get_DropDownSelectedIndex](./get_dropdownselectedindex/)() | يحصل على الفهرس الذي يحدد العنصر المحدد حاليًا في حقل النموذج المنسدل. |
| [get_Enabled](./get_enabled/)() | صحيح إذا كان حقل النموذج مفعلاً. |
| [get_EntryMacro](./get_entrymacro/)() | يرجع أو يضبط اسم ماكرو الدخول لحقل النموذج. |
| [get_ExitMacro](./get_exitmacro/)() | يرجع أو يضبط اسم ماكرو الخروج لحقل النموذج. |
| [get_Font](../../aspose.words/inline/get_font/)() | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| [get_HelpText](./get_helptext/)() | يرجع أو يضبط النص المعروض في مربع الرسالة عندما يكون حقل النموذج في التركيز ويضغط المستخدم F1. |
| [get_IsCheckBoxExactSize](./get_ischeckboxexactsize/)() | يحصل على أو يضبط القيمة المنطقية التي تشير إلى ما إذا كان حجم مربع النص تلقائيًا أم محددًا صراحة. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | يعيد **true** إذا كان بإمكان هذه العقدة احتواء عقد أخرى. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | يرجع true إذا تم حذف هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | يرجع true إذا تم تغيير تنسيق الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | يرجع true إذا تم إدراج هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | يرجع **true** إذا تم نقل (حذف) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | يرجع **true** إذا تم نقل (إدراج) هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً. |
| [get_MaxLength](./get_maxlength/)() | الحد الأقصى للطول لحقل النص. صفر عندما لا يكون الطول محدودًا. |
| [get_Name](./get_name/)() | يحصل على أو يضبط اسم حقل النموذج. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [get_NodeType](./get_nodetype/)() const override | يرجع [FormField](../../aspose.words/nodetype/). |
| [get_OwnHelp](./get_ownhelp/)() | يحدد مصدر النص المعروض في مربع الرسالة عندما يكون حقل النموذج في التركيز ويضغط المستخدم F1. |
| [get_OwnStatus](./get_ownstatus/)() | يحدد مصدر النص المعروض في شريط الحالة عندما يكون حقل النموذج في التركيز. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | يحصل على الوالد المباشر لهذه العقدة. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | يسترجع الفقرة الأب [Paragraph](../../aspose.words/paragraph/) لهذه العقدة. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | يرجع كائن [Range](../../aspose.words/range/) الذي يمثل الجزء من المستند الموجود داخل هذه العقدة. |
| [get_Result](./get_result/)() | يحصل على أو يضبط سلسلة تمثل نتيجة هذا الحقل النموذج. |
| [get_StatusText](./get_statustext/)() | يرجع أو يضبط النص المعروض في شريط الحالة عندما يكون حقل النموذج في التركيز. |
| [get_TextInputDefault](./get_textinputdefault/)() | يحصل على أو يضبط السلسلة الافتراضية أو تعبير الحساب لحقل نموذج نصي. |
| [get_TextInputFormat](./get_textinputformat/)() | يرجع أو يضبط تنسيق النص لحقل نموذج نصي. |
| [get_TextInputType](./get_textinputtype/)() | يحصل على نوع حقل نموذج نصي. |
| [get_Type](./get_type/)() | يرجع نوع حقل النموذج. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | يحصل على السلف الأول من النوع المحدد [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetText](../../aspose.words/specialchar/gettext/)() override | يحصل على الحرف الخاص الذي تمثله هذه العقدة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة التالية وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة صديقة للمستخدم. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور الشجرة بترتيب ما قبل الترتيب. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من العنصر الأب. |
| [RemoveField](./removefield/)() | يزيل حقل النموذج بالكامل، وليس مجرد الحرف الخاص بحقل النموذج. |
| [set_CalculateOnExit](./set_calculateonexit/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FormField::get_CalculateOnExit](./get_calculateonexit/). |
| [set_CheckBoxSize](./set_checkboxsize/)(double) | مُعيّن لـ [Aspose::Words::Fields::FormField::get_CheckBoxSize](./get_checkboxsize/). |
| [set_Checked](./set_checked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FormField::get_Checked](./get_checked/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Default](./set_default/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FormField::get_Default](./get_default/). |
| [set_DropDownSelectedIndex](./set_dropdownselectedindex/)(int32_t) | يضبط الفهرس الذي يحدد العنصر المحدد حاليًا في حقل النموذج المنسدل. |
| [set_Enabled](./set_enabled/)(bool) | صحيح إذا كان حقل النموذج مفعلاً. |
| [set_EntryMacro](./set_entrymacro/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FormField::get_EntryMacro](./get_entrymacro/). |
| [set_ExitMacro](./set_exitmacro/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FormField::get_ExitMacro](./get_exitmacro/). |
| [set_HelpText](./set_helptext/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FormField::get_HelpText](./get_helptext/). |
| [set_IsCheckBoxExactSize](./set_ischeckboxexactsize/)(bool) | المُعيّن لـ [Aspose::Words::Fields::FormField::get_IsCheckBoxExactSize](./get_ischeckboxexactsize/). |
| [set_MaxLength](./set_maxlength/)(int32_t) | الحد الأقصى للطول لحقل النص. صفر عندما لا يكون الطول محدودًا. |
| [set_Name](./set_name/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FormField::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_OwnHelp](./set_ownhelp/)(bool) | المُعيّن لـ [Aspose::Words::Fields::FormField::get_OwnHelp](./get_ownhelp/). |
| [set_OwnStatus](./set_ownstatus/)(bool) | المُعيّن لـ [Aspose::Words::Fields::FormField::get_OwnStatus](./get_ownstatus/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Result](./set_result/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FormField::get_Result](./get_result/). |
| [set_StatusText](./set_statustext/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FormField::get_StatusText](./get_statustext/). |
| [set_TextInputDefault](./set_textinputdefault/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FormField::get_TextInputDefault](./get_textinputdefault/). |
| [set_TextInputFormat](./set_textinputformat/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FormField::get_TextInputFormat](./get_textinputformat/). |
| [set_TextInputType](./set_textinputtype/)(Aspose::Words::Fields::TextFormFieldType) | يحدد نوع حقل نموذج نصي. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTextInputValue](./settextinputvalue/)(const System::SharedPtr\<System::Object\>\&) | يطبق تنسيق النص المحدد في [TextInputFormat](./get_textinputformat/) ويخزن القيمة في [Result](./get_result/). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | يصدّر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | يصدّر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [Type](./type/)() |  |
## ملاحظات


يقدم Microsoft Word حقول النماذج التالية: مربع اختيار، إدخال نص، وقائمة منسدلة (قائمة منسدلة).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and positioned as a character within a line of text.

حقل نموذج كامل في مستند Word هو بنية معقدة تمثلها عدة عقد: بداية الحقل، رمز الحقل مثل FORMTEXT، بيانات حقل النموذج، فاصل الحقل، نتيجة الحقل، نهاية الحقل وإشارة مرجعية. لإنشاء حقول نماذج برمجيًا في مستند Word استخدم [InsertCheckBox()](../)، [InsertTextInput()](../) و[InsertComboBox()](../) التي تضمن إنشاء جميع عقد حقل النموذج بترتيب صحيح وفي حالة مناسبة.

## أمثلة



يوضح كيفية إدراج مربع اختيار.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// أدرج مربع اختيار يتيح للمستخدم اختيار خيار من مجموعة من السلاسل.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// سيظهر حقل النموذج على شكل وسم HTML "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```


يوضح كيفية تنسيق كامل [FormField](./)، بما في ذلك قيمة الحقل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(0);
formField->get_Font()->set_Bold(true);
formField->get_Font()->set_Size(24);
formField->get_Font()->set_Color(System::Drawing::Color::get_Red());

formField->set_Result(u"Aspose.FormField");

doc = Aspose::Words::ApiExamples::DocumentHelper::SaveOpen(doc);

System::SharedPtr<Aspose::Words::Run> formFieldRun = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1);

ASSERT_EQ(u"Aspose.FormField", formFieldRun->get_Text());
ASPOSE_ASSERT_EQ(true, formFieldRun->get_Font()->get_Bold());
ASPOSE_ASSERT_EQ(24, formFieldRun->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), formFieldRun->get_Font()->get_Color().ToArgb());
```

## انظر أيضًا

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
