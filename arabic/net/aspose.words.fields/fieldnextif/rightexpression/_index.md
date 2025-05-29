---
title: FieldNextIf.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldNextIf RightExpression لإدارة الجانب الأيمن من تعبيرات المقارنة وتخصيصه بسهولة لتحسين التعامل مع البيانات.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldnextif/rightexpression/
---
## FieldNextIf.RightExpression property

يحصل على الجزء الصحيح من تعبير المقارنة أو يعينه.

```csharp
public string RightExpression { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول NEXT/NEXTIF لدمج صفوف متعددة في صفحة واحدة أثناء دمج البريد.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // قم بإنشاء مصدر بيانات لدمج البريد الخاص بنا مع 3 صفوف.
    // سيؤدي دمج البريد الذي يستخدم هذا الجدول عادةً إلى إنشاء مستند مكون من 3 صفحات.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // إذا كان لدينا حقول دمج متعددة بنفس اسم الحقل،
    // سوف يتلقون البيانات من نفس الصف الخاص بمصدر البيانات ويعرضون نفس القيمة بعد الدمج.
    // يخبر الحقل التالي دمج البريد بالانتقال لأسفل صفًا واحدًا على الفور،
    // وهذا يعني أن أي MERGEFIELDs التي تأتي بعد الحقل NEXT ستستقبل البيانات من الصف التالي.
    // تأكد من عدم محاولة الانتقال إلى الصف التالي أبدًا أثناء وجودك بالفعل في الصف الأخير.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // بعد الدمج، قيم مصدر البيانات التي تقبلها حقول الدمج هذه
     // سوف ينتهي الأمر في نفس الصفحة مثل MERGEFIELDs أعلاه.
    InsertMergeFields(builder, "Second row: ");

    // حقل NEXTIF له نفس وظيفة حقل NEXT،
    // لكنه ينتقل إلى الصف التالي فقط إذا كانت العبارة التي تم إنشاؤها بواسطة الخصائص الثلاث التالية صحيحة.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // إذا كانت المقارنة التي تم تأكيدها بواسطة الحقل أعلاه صحيحة،
    // ستأخذ حقول الدمج الثلاثة التالية البيانات من الصف الثالث.
    // وإلا، فسوف تأخذ هذه الحقول البيانات من الصف الثاني مرة أخرى.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     //يحتوي مصدر البيانات لدينا على 3 صفوف، وقد تخطينا الصفوف مرتين.
    // ستحتوي مستندنا الناتج على صفحة واحدة تحتوي على بيانات من جميع الصفوف الثلاثة.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج MERGEFIELDs لمصدر البيانات الذي يحتوي على أعمدة تسمى "اللقب المجاملة" و"الاسم الأول" و"الاسم الأخير".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج MERRGEFIELD بالخصائص المحددة.
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
