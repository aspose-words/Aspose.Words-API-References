---
title: FieldGreetingLine Class
linktitle: FieldGreetingLine
articleTitle: FieldGreetingLine
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldGreetingLine، المصممة لتنفيذ حقول GREETINGLINE بسهولة لتحسين تخصيص المستندات.
type: docs
weight: 2390
url: /ar/net/aspose.words.fields/fieldgreetingline/
---
## FieldGreetingLine class

ينفذ حقل GREETINGLINE.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldGreetingLine : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldGreetingLine](fieldgreetingline/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AlternateText](../../aspose.words.fields/fieldgreetingline/alternatetext/) { get; set; } | يحصل على النص الذي سيتم تضمينه في الحقل أو يعينه إذا كان الاسم فارغًا. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LanguageId](../../aspose.words.fields/fieldgreetingline/languageid/) { get; set; } | يحصل على معرف اللغة المستخدم لتنسيق الاسم أو يعينه. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [NameFormat](../../aspose.words.fields/fieldgreetingline/nameformat/) { get; set; } | يحصل على تنسيق الاسم المضمن في الحقل أو يعينه. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetFieldNames](../../aspose.words.fields/fieldgreetingline/getfieldnames/)() | يعيد مجموعة من أسماء حقول دمج البريد التي يستخدمها الحقل. |
| [Remove](../../aspose.words.fields/field/remove/)() | يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يُجري تحديث الحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | يُجري تحديثًا للحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |

## ملاحظات

يقوم بإدراج سطر تحية دمج البريد.

## أمثلة

يوضح كيفية إدراج حقل GREETINGLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء تحية عامة باستخدام حقل GREETINGLINE، وبعض النص بعده.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// يقبل حقل GREETINGLINE القيم من مصدر البيانات أثناء دمج البريد، مثل MERGEFIELD.
// ويمكنه أيضًا تنسيق كيفية كتابة بيانات المصدر في مكانها بمجرد اكتمال دمج البريد.
// تتوافق مجموعة أسماء الحقول مع الأعمدة من مصدر البيانات
// أن الحقل سوف يأخذ القيم منه.
Assert.AreEqual(0, field.GetFieldNames().Length);

//لملء هذه المصفوفة، نحتاج إلى تحديد تنسيق لسطر التحية الخاص بنا.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// الآن، سيقبل حقلنا القيم من هذين العمودين في مصدر البيانات.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// سيغطي هذا السلسلة أي حالات تكون فيها بيانات جدول البيانات غير صالحة
// عن طريق استبدال الاسم المشوه بسلسلة.
field.AlternateText = "Sir or Madam";

// تعيين الإعدادات المحلية لتنسيق النتيجة.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// إنشاء جدول بيانات يحتوي على أعمدة تتطابق أسماؤها مع العناصر
// من مجموعة أسماء حقول الحقل، ثم قم بتنفيذ دمج البريد.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// يحتوي هذا الصف على قيمة غير صالحة في عمود عنوان المجاملة، لذا سيتم تعيين تحيتنا افتراضيًا على النص البديل.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.AreEqual(0, doc.Range.Fields.Count);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
