---
title: Class FormField
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FormField فصل. يمثل حقل نموذج واحد.
type: docs
weight: 2620
url: /ar/net/aspose.words.fields/formfield/
---
## FormField class

يمثل حقل نموذج واحد.

لمعرفة المزيد، قم بزيارة[العمل مع حقول النموذج](https://docs.aspose.com/words/net/working-with-form-fields/) مقالة توثيقية.

```csharp
public class FormField : SpecialChar
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | صحيح إذا تم تحديث المراجع إلى حقل النموذج المحدد تلقائيًا عند الخروج من الحقل. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | الحصول على حجم مربع الاختيار أو تحديده بالنقاط. يكون له تأثير فقط عندما[`IsCheckBoxExactSize`](./ischeckboxexactsize/) يكون`حقيقي` . |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | الحصول على الحالة المحددة لحقل نموذج خانة الاختيار أو تعيينها. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | الحصول على القيمة الافتراضية لحقل نموذج خانة الاختيار أو تعيينها. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | يوفر الوصول إلى عناصر حقل النموذج المنسدل. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | الحصول على أو تعيين الفهرس الذي يحدد العنصر المحدد حاليًا في حقل نموذج القائمة المنسدلة. |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | صحيح إذا تم تمكين حقل النموذج. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | إرجاع أو تعيين اسم ماكرو الإدخال لحقل النموذج. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | إرجاع أو تعيين اسم ماكرو للخروج لحقل النموذج. |
| [Font](../../aspose.words/inline/font/) { get; } | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | إرجاع أو تعيين النص المعروض في مربع رسالة عندما يكون حقل النموذج هو التركيز ويقوم المستخدم بالضغط على F1. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | الحصول على أو تعيين القيمة المنطقية التي تشير إلى ما إذا كان حجم مربع النص تلقائيًا أو محددًا بشكل صريح. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | الحد الأقصى لطول حقل النص. صفر عندما لا يكون الطول محدودًا. |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | الحصول على اسم حقل النموذج أو تعيينه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | إرجاعFormField . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | يحدد مصدر النص الذي يتم عرضه في مربع رسالة عندما يكون التركيز على حقل النموذج ويقوم المستخدم بالضغط على F1. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | يحدد مصدر النص الذي يتم عرضه في شريط الحالة عندما يكون حقل النموذج هو التركيز. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../../aspose.words/paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../../aspose.words/range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | الحصول على أو تعيين سلسلة تمثل نتيجة حقل النموذج هذا. |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | إرجاع أو تعيين النص المعروض في شريط الحالة عندما يكون حقل النموذج هو التركيز. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | الحصول على أو تعيين السلسلة الافتراضية أو تعبير الحساب لحقل نموذج نصي. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | إرجاع أو تعيين تنسيق النص لحقل نموذج نصي. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | الحصول على أو تعيين نوع حقل النموذج النصي. |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | إرجاع نوع حقل النموذج. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(DocumentVisitor) | يقبل الزائر. |
| [Clone](../../aspose.words/node/clone/)(bool) | إنشاء نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على السلف الأول للمحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على السلف الأول لنوع الكائن المحدد. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | الحصول على الحرف الخاص الذي تمثله هذه العقدة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | إزالة حقل النموذج بالكامل، وليس فقط الحرف الخاص لحقل النموذج. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(object) | يطبق تنسيق النص المحدد في[`TextInputFormat`](./textinputformat/) ويخزن القيمة فيها[`Result`](./result/) . |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

يوفر Microsoft Word حقول النموذج التالية: مربع الاختيار وإدخال النص والقائمة المنسدلة (مربع التحرير والسرد).

`FormField`هي عقدة مضمّنة ويمكن أن تكون تابعة فقط لـ[`Paragraph`](../../aspose.words/paragraph/).

`FormField` يتم تمثيله في المستند بحرف خاص و يتم وضعه كحرف داخل سطر من النص.

يعد حقل النموذج الكامل في مستند Word عبارة عن بنية معقدة يتم تمثيلها بعدة عقد : بداية الحقل، ورمز الحقل مثل FORMTEXT، وبيانات حقل النموذج، وفاصل الحقل، ونتيجة الحقل ، ونهاية الحقل، والإشارة المرجعية. لإنشاء حقول نموذج برمجياً في مستند Word، استخدم [`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/)[`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) و [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/) who تأكد من إنشاء كافة عقد حقل النموذج بالترتيب الصحيح وفي الحالة المناسبة.

### أمثلة

يوضح كيفية تنسيق FormField بأكمله، بما في ذلك قيمة الحقل.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[0];
formField.Font.Bold = true;
formField.Font.Size = 24;
formField.Font.Color = Color.Red;

formField.Result = "Aspose.FormField";

doc = DocumentHelper.SaveOpen(doc);

Run formFieldRun = doc.FirstSection.Body.FirstParagraph.Runs[1];

Assert.AreEqual("Aspose.FormField", formFieldRun.Text);
Assert.AreEqual(true, formFieldRun.Font.Bold);
Assert.AreEqual(24, formFieldRun.Font.Size);
Assert.AreEqual(Color.Red.ToArgb(), formFieldRun.Font.Color.ToArgb());
```

يوضح كيفية إدراج مربع التحرير والسرد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// أدخل مربع التحرير والسرد الذي سيسمح للمستخدم باختيار خيار من مجموعة من السلاسل.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// سيظهر حقل النموذج على شكل علامة html "تحديد".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### أنظر أيضا

* class [SpecialChar](../../aspose.words/specialchar/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


