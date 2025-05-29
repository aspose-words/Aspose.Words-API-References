---
title: FormField Class
linktitle: FormField
articleTitle: FormField
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FormField لإنشاء حقول نماذج قابلة للتخصيص وإدارتها بسهولة في مستنداتك لتحسين تفاعل المستخدم.
type: docs
weight: 3030
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
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | يحصل على حجم مربع الاختيار بالنقاط أو يضبطه. يسري فقط عند[`IsCheckBoxExactSize`](./ischeckboxexactsize/) يكون`حقيقي` . |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | يحصل على حالة التحقق لحقل نموذج مربع الاختيار أو يعينها. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | يحصل على القيمة الافتراضية لحقل نموذج مربع الاختيار أو يعينها. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | يوفر الوصول إلى عناصر حقل نموذج القائمة المنسدلة. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | يحصل على الفهرس الذي يحدد العنصر المحدد حاليًا في حقل نموذج القائمة المنسدلة أو يعينه. |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | صحيح إذا تم تمكين حقل النموذج. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | يقوم بإرجاع أو تعيين اسم ماكرو الإدخال لحقل النموذج. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | يعيد أو يعين اسم ماكرو الخروج لحقل النموذج. |
| [Font](../../aspose.words/inline/font/) { get; } | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | يعيد أو يعين النص الذي يتم عرضه في مربع الرسالة عندما يكون حقل النموذج هو موضع التركيز ويضغط المستخدم على F1. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | يحصل على القيمة المنطقية التي تشير إلى ما إذا كان حجم مربع النص تلقائيًا أو محددًا صراحةً أو يعينها. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة قادرة على احتواء عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | يعود صحيحًا إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | يعود صحيحًا إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | الحد الأقصى لطول حقل النص. صفر عندما لا يكون الطول محدودًا. |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | يحصل على اسم حقل النموذج أو يعينه. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | إرجاعFormField . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | يحدد مصدر النص الذي يتم عرضه في مربع الرسالة عندما يكون حقل النموذج هو موضع التركيز ويضغط المستخدم على F1. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | يحدد مصدر النص الذي يتم عرضه في شريط الحالة عندما يكون حقل النموذج هو محور التركيز. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../../aspose.words/paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../../aspose.words/range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | يحصل على سلسلة تمثل نتيجة حقل النموذج هذا أو يعينها. |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | يقوم بإرجاع أو تعيين النص الذي يتم عرضه في شريط الحالة عندما يكون حقل النموذج هو موضع التركيز. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | يحصل على السلسلة الافتراضية أو تعبير حساب لحقل نموذج نصي أو يعينه. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | يعيد أو يعين تنسيق النص لحقل نموذج النص. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | يحصل على نوع حقل نموذج النص أو يعينه. |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | يعيد نوع حقل النموذج. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | يحصل على الحرف الخاص الذي تمثله هذه العقدة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | يزيل حقل النموذج بالكامل، وليس فقط الحرف الخاص بحقل النموذج. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(*object*) | يطبق تنسيق النص المحدد في[`TextInputFormat`](./textinputformat/) ويخزن القيمة في[`Result`](./result/) . |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

يوفر Microsoft Word حقول النموذج التالية: مربع الاختيار، وإدخال النص، والقائمة المنسدلة (المربع المنسدل).

`FormField` هي عقدة مضمنة ولا يمكن أن تكون إلا طفلة لـ[`Paragraph`](../../aspose.words/paragraph/).

`FormField` يتم تمثيله في المستند بحرف خاص و يتم وضعه كحرف داخل سطر من النص.

حقل النموذج الكامل في مستند وورد هو بنية معقدة تُمثَّل بعدة عقد x000d_: بداية الحقل، رمز الحقل مثل FORMTEXT، بيانات حقل النموذج، فاصل الحقل، نتيجة حقل x000d_، نهاية الحقل، وعلامة مرجعية. لإنشاء حقول نموذج برمجيًا في مستند وورد، استخدم x000d_[`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/) ، [`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) و [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/)which تأكد من إنشاء جميع عقد حقول النموذج بالترتيب الصحيح وفي حالة مناسبة.

## أمثلة

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

يوضح كيفية إدراج مربع المجموعة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// أدخل مربعًا مركبًا يسمح للمستخدم باختيار خيار من مجموعة من السلاسل.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

//سيظهر حقل النموذج في شكل علامة HTML "select".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### أنظر أيضا

* class [SpecialChar](../../aspose.words/specialchar/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
