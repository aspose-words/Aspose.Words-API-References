---
title: FieldGreetingLine
second_title: Aspose.Words لمراجع .NET API
description: تنفيذ حقل الخط الأخضر .
type: docs
weight: 1830
url: /ar/net/aspose.words.fields/fieldgreetingline/
---
## FieldGreetingLine class

تنفيذ حقل الخط الأخضر .

```csharp
public class FieldGreetingLine : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldGreetingLine](fieldgreetingline)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AlternateText](../../aspose.words.fields/fieldgreetingline/alternatetext) { get; set; } | الحصول على أو تعيين النص المراد تضمينه في الحقل إذا كان الاسم فارغًا. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format) { get; } | يحصل على أ[`FieldFormat`](../fieldformat) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LanguageId](../../aspose.words.fields/fieldgreetingline/languageid) { get; set; } | الحصول على أو تعيين معرّف اللغة المستخدم لتنسيق الاسم. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [NameFormat](../../aspose.words.fields/fieldgreetingline/nameformat) { get; set; } | الحصول على تنسيق الاسم المضمن في الحقل أو تعيينه. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [GetFieldNames](../../aspose.words.fields/fieldgreetingline/getfieldnames)() | إرجاع مجموعة من أسماء حقول دمج المراسلات المستخدمة بواسطة الحقل. |
| [Remove](../../aspose.words.fields/field/remove)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

إدراج سطر ترحيب دمج المراسلات .

### أمثلة

يوضح كيفية إدراج حقل GREETINGLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أنشئ تحية عامة باستخدام حقل GREETINGLINE ، وبعض النص بعده.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// يقبل حقل GREETINGLINE القيم من مصدر بيانات أثناء دمج البريد ، مثل MERGEFIELD.
// يمكنه أيضًا تنسيق كيفية كتابة بيانات المصدر في مكانها بمجرد اكتمال دمج البريد.
// تتوافق مجموعة أسماء الحقول مع الأعمدة من مصدر البيانات
// التي سيأخذ منها الحقل قيمًا.
Assert.AreEqual(0, field.GetFieldNames().Length);

// لتعبئة هذه المصفوفة ، نحتاج إلى تحديد تنسيق لسطر الترحيب الخاص بنا.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// الآن ، سيقبل حقلنا القيم من هذين العمودين في مصدر البيانات.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// ستغطي هذه السلسلة أي حالات تكون فيها بيانات جدول البيانات غير صالحة
// عن طريق استبدال الاسم المشوه بسلسلة.
field.AlternateText = "Sir or Madam";

// قم بتعيين لغة لتنسيق النتيجة.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// أنشئ جدول بيانات بأعمدة تتطابق أسماؤها مع العناصر
// من مجموعة أسماء الحقول الخاصة بالحقل ، ثم قم بتنفيذ عملية دمج البريد.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// يحتوي هذا الصف على قيمة غير صالحة في عمود عنوان المجاملة ، لذا فإن تحياتنا ستتحول إلى النص البديل افتراضيًا.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields, Is.Empty);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### أنظر أيضا

* class [Field](../field)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
