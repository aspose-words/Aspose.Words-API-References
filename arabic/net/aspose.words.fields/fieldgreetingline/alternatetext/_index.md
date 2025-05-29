---
title: FieldGreetingLine.AlternateText
linktitle: AlternateText
articleTitle: AlternateText
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية AlternateText FieldGreetingLine لتحسين تجربة المستخدم من خلال عرض نص مخصص عند فقدان الأسماء.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldgreetingline/alternatetext/
---
## FieldGreetingLine.AlternateText property

يحصل على النص الذي سيتم تضمينه في الحقل أو يعينه إذا كان الاسم فارغًا.

```csharp
public string AlternateText { get; set; }
```

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

* class [FieldGreetingLine](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
