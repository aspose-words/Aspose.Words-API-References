---
title: FieldChar
second_title: Aspose.Words لمراجع .NET API
description: الفئة الأساسية للعقد التي تمثل أحرف الحقل في مستند.
type: docs
weight: 1520
url: /ar/net/aspose.words.fields/fieldchar/
---
## FieldChar class

الفئة الأساسية للعقد التي تمثل أحرف الحقل في مستند.

```csharp
public abstract class FieldChar : SpecialChar
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص . |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | إرجاع نوع الحقل. |
| [Font](../../aspose.words/inline/font/) { get; } | يوفر الوصول إلى تنسيق خط هذا الكائن. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع صحيح إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | الحصول على أو تحديد ما إذا كان الحقل الأصلي مغلقًا (يجب عدم إعادة حساب النتيجة) . |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | عوائد **حقيقي** إذا تم نقل (حذف) هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | عوائد **حقيقي** إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغيير. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | عوائد **NodeType.SpecialChar** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | استرداد الأصل[`Paragraph`](../../aspose.words/paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/specialchar/accept/)(DocumentVisitor) | يقبل الزائر . |
| [Clone](../../aspose.words/node/clone/)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | إرجاع حقل للحقل char . |
| override [GetText](../../aspose.words/specialchar/gettext/)() | يحصل على الحرف الخاص الذي تمثله هذه العقدة . |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

الحقل الكامل في مستند Microsoft Word عبارة عن بنية معقدة تتكون من حرف بداية الحقل ، ورمز الحقل ، وحرف فاصل الحقل ، ونتائج الحقل وحرف نهاية الحقل. تحتوي بعض الحقول فقط على بداية الحقل ورمز الحقل ونهاية الحقل.

لإدراج حقل جديد بسهولة في مستند ، استخدم ملحق[`InsertField`](../../aspose.words/documentbuilder/insertfield/) طريقة .

### أمثلة

يوضح كيفية العمل مع عقدة FieldStart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// استرجع كائن الواجهة الذي يمثل الحقل في المستند.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// تحديث الحقل لإظهار التاريخ الحالي.
field.Update();
```

### أنظر أيضا

* class [FieldStart](../fieldstart/)
* class [FieldSeparator](../fieldseparator/)
* class [FieldEnd](../fieldend/)
* class [SpecialChar](../../aspose.words/specialchar/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
