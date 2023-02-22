---
title: FieldGreetingLine.NameFormat
second_title: Aspose.Words لمراجع .NET API
description: FieldGreetingLine ملكية. الحصول على تنسيق الاسم المضمن في الحقل أو تعيينه.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldgreetingline/nameformat/
---
## FieldGreetingLine.NameFormat property

الحصول على تنسيق الاسم المضمن في الحقل أو تعيينه.

```csharp
public string NameFormat { get; set; }
```

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

* class [FieldGreetingLine](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldgreetingline/)
* المجسم [Aspose.Words](../../../)


