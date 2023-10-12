---
title: Class FieldInclude
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldInclude فصل. ينفذ الحقل INCLUDE.
type: docs
weight: 2030
url: /ar/net/aspose.words.fields/fieldinclude/
---
## FieldInclude class

ينفذ الحقل INCLUDE.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldInclude : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldInclude](fieldinclude/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldinclude/bookmarkname/) { get; set; } | الحصول على أو تعيين اسم الإشارة المرجعية في المستند المراد تضمينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [LockFields](../../aspose.words.fields/fieldinclude/lockfields/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم منع تحديث الحقول الموجودة في المستند المضمن. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [SourceFullName](../../aspose.words.fields/fieldinclude/sourcefullname/) { get; set; } | الحصول على أو تعيين موقع المستند. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [TextConverter](../../aspose.words.fields/fieldinclude/textconverter/) { get; set; } | الحصول على أو تعيين اسم محول النص لتنسيق الملف المضمن. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

إدراج كل أو جزء من النص والرسومات الموجودة في مستند آخر.

### أمثلة

يوضح كيفية إنشاء حقل INCLUDE وتعيين خصائصه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا استخدام حقل INCLUDE لاستيراد جزء من مستند آخر في نظام الملفات المحلي.
// تحتوي الإشارة المرجعية من المستند الآخر الذي نشير إليه بهذا الحقل على هذا الجزء المستورد.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


