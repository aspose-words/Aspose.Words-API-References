---
title: FieldChar Class
linktitle: FieldChar
articleTitle: FieldChar
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldChar، القاعدة الأساسية لأحرف حقول المستند، والتي تعمل على تحسين معالجة المستندات وتخصيصها.
type: docs
weight: 2080
url: /ar/net/aspose.words.fields/fieldchar/
---
## FieldChar class

الفئة الأساسية للعقد التي تمثل أحرف الحقل في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public abstract class FieldChar : SpecialChar
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | يعيد نوع الحقل. |
| [Font](../../aspose.words/inline/font/) { get; } | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة قادرة على احتواء عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | يعود صحيحًا إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | يحصل على أو يعين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | يعود صحيحًا إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | يعود صحيحًا إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل الرئيسي مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تتبع التغييرات. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | إرجاعSpecialChar . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../../aspose.words/paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../../aspose.words/range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words/specialchar/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل زائرًا. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | يعيد حقلًا لحقل char. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | يحصل على الحرف الخاص الذي تمثله هذه العقدة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

الحقل الكامل في مستند مايكروسوفت وورد هو بنية معقدة تتكون من حرف بداية الحقل، ورمز الحقل، وحرف فاصل الحقل، ونتيجة الحقل x000d، وحرف نهاية الحقل. بعض الحقول تحتوي فقط على بداية الحقل، ورمز الحقل، ونهاية الحقل.

لإدراج حقل جديد بسهولة في مستند، استخدم[`InsertField`](../../aspose.words/documentbuilder/insertfield/) طريقة .

## أمثلة

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

// استرداد كائن الواجهة الذي يمثل الحقل في المستند.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

//تحديث الحقل لإظهار التاريخ الحالي.
field.Update();
```

### أنظر أيضا

* class [FieldStart](../fieldstart/)
* class [FieldSeparator](../fieldseparator/)
* class [FieldEnd](../fieldend/)
* class [SpecialChar](../../aspose.words/specialchar/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
