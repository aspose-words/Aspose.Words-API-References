---
title: FieldNextIf.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words لـ .NET
description: FieldNextIf RightExpression ملكية. الحصول على أو تعيين الجزء الأيمن من تعبير المقارنة في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldnextif/rightexpression/
---
## FieldNextIf.RightExpression property

الحصول على أو تعيين الجزء الأيمن من تعبير المقارنة.

```csharp
public string RightExpression { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول NEXT/NEXTIF لدمج صفوف متعددة في صفحة واحدة أثناء عملية دمج البريد.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أنشئ مصدر بيانات لدمج البريد لدينا بثلاثة صفوف.
    // عادةً ما يؤدي دمج البريد الذي يستخدم هذا الجدول إلى إنشاء مستند من 3 صفحات.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // إذا كان لدينا حقول دمج متعددة بنفس اسم الحقل،
    // سوف يتلقون البيانات من نفس الصف من مصدر البيانات ويعرضون نفس القيمة بعد الدمج.
    // يخبر الحقل التالي دمج المراسلات على الفور بالتحرك لأسفل صفًا واحدًا،
    // مما يعني أن أي MERGEFIELDs تتبع الحقل التالي ستتلقى بيانات من الصف التالي.
    // تأكد من عدم محاولة الانتقال إلى الصف التالي مطلقًا أثناء وجودك في الصف الأخير.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // بعد الدمج، قيم مصدر البيانات التي تقبلها وحدات MERGEFIELD هذه
     // سينتهي في نفس الصفحة مثل MERGEFIELDs أعلاه.
    InsertMergeFields(builder, "Second row: ");

    // الحقل NEXTIF له نفس وظيفة الحقل التالي،
    // ولكنه ينتقل إلى الصف التالي فقط إذا كانت العبارة التي تم إنشاؤها بواسطة الخصائص الثلاث التالية صحيحة.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // إذا كانت المقارنة التي يؤكدها الحقل أعلاه صحيحة،
    // ستأخذ حقول الدمج الثلاثة التالية البيانات من الصف الثالث.
    // بخلاف ذلك، ستأخذ هذه الحقول البيانات من الصف 2 مرة أخرى.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // يحتوي مصدر البيانات لدينا على 3 صفوف، وقمنا بتخطي الصفوف مرتين.
    // سيحتوي مستند الإخراج الخاص بنا على صفحة واحدة تحتوي على بيانات من جميع الصفوف الثلاثة.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج MERGEFIELDs لمصدر بيانات يحتوي على أعمدة تسمى "عنوان الخدمة" و"الاسم الأول" و"اسم العائلة".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج MERRGEFIELD بخصائص محددة.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### أنظر أيضا

* class [FieldNextIf](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
