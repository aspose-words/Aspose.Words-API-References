---
title: Class FieldHyperlink
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldHyperlink فصل. تنفذ الحقل HYPERLINK
type: docs
weight: 1840
url: /ar/net/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class

تنفذ الحقل HYPERLINK

```csharp
public class FieldHyperlink : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldHyperlink](fieldhyperlink/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Address](../../aspose.words.fields/fieldhyperlink/address/) { get; set; } | الحصول على أو تعيين موقع حيث ينتقل هذا الارتباط التشعبي. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsImageMap](../../aspose.words.fields/fieldhyperlink/isimagemap/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إلحاق إحداثيات بالارتباط التشعبي لخريطة صورة من جانب الخادم. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [OpenInNewWindow](../../aspose.words.fields/fieldhyperlink/openinnewwindow/) { get; set; } | يحصل أو يحدد ما إذا كان سيتم فتح الموقع الوجهة في نافذة مستعرض ويب جديدة. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [ScreenTip](../../aspose.words.fields/fieldhyperlink/screentip/) { get; set; } | الحصول على نص تلميح الشاشة للارتباط التشعبي أو تعيينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [SubAddress](../../aspose.words.fields/fieldhyperlink/subaddress/) { get; set; } | الحصول على أو تعيين موقع في الملف ، مثل إشارة مرجعية ، حيث ينتقل هذا الارتباط التشعبي. |
| [Target](../../aspose.words.fields/fieldhyperlink/target/) { get; set; } | الحصول على أو تحديد الهدف الذي يجب إعادة توجيه الارتباط إليه. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove/)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

عند تحديده ، يتسبب في انتقال التحكم إلى الموقع مثل إشارة مرجعية أو عنوان URL.

### أمثلة

يوضح كيفية استخدام حقول HYPERLINK للارتباط بالمستندات في نظام الملفات المحلي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// عندما نضغط على حقل HYPERLINK هذا في Microsoft Word ،
// سيفتح المستند المرتبط ثم يضع المؤشر على الإشارة المرجعية المحددة.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// عندما نضغط على حقل HYPERLINK هذا في Microsoft Word ،
// سيفتح المستند المرتبط ، وينتقل تلقائيًا لأسفل إلى إطار iframe المحدد.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


