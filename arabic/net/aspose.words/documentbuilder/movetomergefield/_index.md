---
title: DocumentBuilder.MoveToMergeField
linktitle: MoveToMergeField
articleTitle: MoveToMergeField
second_title: Aspose.Words لـ .NET
description: DocumentBuilder MoveToMergeField طريقة. يحرك المؤشر إلى موضع يقع خارج حقل الدمج المحدد مباشرة ويزيل حقل الدمج في C#.
type: docs
weight: 550
url: /ar/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(*string*) {#movetomergefield}

يحرك المؤشر إلى موضع يقع خارج حقل الدمج المحدد مباشرة ويزيل حقل الدمج.

```csharp
public bool MoveToMergeField(string fieldName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldName | String | الاسم غير حساس لحالة الأحرف لحقل دمج المراسلات. |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على حقل الدمج وتم نقل المؤشر؛`خطأ شنيع` خلاف ذلك.

## ملاحظات

لاحظ أن هذه الطريقة تحذف حقل الدمج من المستند بعد تحريك المؤشر.

## أمثلة

يوضح كيفية تعبئة MERGEFIELDs بالبيانات باستخدام منشئ المستندات بدلاً من دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل بعض حقول MERGEFIELDS، التي تقبل البيانات من الأعمدة التي تحمل نفس الاسم في مصدر بيانات أثناء دمج البريد،
// ثم املأها يدويًا.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

يوضح كيفية إدراج حقول نموذج خانة الاختيار في MERGEFIELDs كبيانات دمج أثناء دمج البريد.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // استخدم MERGEFIELDs مع علامات "TableStart"/"TableEnd" لتحديد منطقة دمج البريد
    // الذي ينتمي إلى مصدر بيانات يسمى "StudentCourse" ويحتوي على MERGEFIELD الذي يقبل البيانات من عمود يسمى "CourseName".
    builder.StartTable();
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableStart:StudentCourse ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  CourseName ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableEnd:StudentCourse ");
    builder.EndTable();

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertCheckBox();

    DataTable dataTable = GetStudentCourseDataTable();

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMergeEvent.InsertCheckBox.docx");
}

/// <summary>
/// عند مواجهة MERGEFIELD باسم محدد، يتم إدراج حقل نموذج خانة الاختيار بدلاً من نص دمج البيانات.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// يتم الاتصال به عندما يقوم دمج البريد بدمج البيانات في MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName == "CourseName")
        {
            Assert.AreEqual("StudentCourse", args.TableName);

            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.FieldName);
            builder.InsertCheckBox(args.DocumentFieldName + mCheckBoxCount, false, 0);

            string fieldValue = args.FieldValue.ToString();

            // في هذه الحالة، لكل فهرس سجل 'n'، تكون قيمة الحقل المقابل هي "Course n".
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // لا تفعل شيئا.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// إنشاء مصدر بيانات لدمج المراسلات.
/// </summary>
private static DataTable GetStudentCourseDataTable()
{
    DataTable dataTable = new DataTable("StudentCourse");
    dataTable.Columns.Add("CourseName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Course " + i;
    }

    return dataTable;
}
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## MoveToMergeField(*string, bool, bool*) {#movetomergefield_1}

ينقل حقل الدمج إلى حقل الدمج المحدد.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldName | String | الاسم غير حساس لحالة الأحرف لحقل دمج المراسلات. |
| isAfter | Boolean | متى`حقيقي` ، يحرك المؤشر ليكون بعد نهاية الحقل. متى`خطأ شنيع` ، يحرك المؤشر ليكون قبل بدء الحقل. |
| isDeleteField | Boolean | متى`حقيقي`، يحذف حقل الدمج. |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على حقل الدمج وتم نقل المؤشر؛`خطأ شنيع` خلاف ذلك.

## أمثلة

يوضح كيفية إدراج الحقول وتحريك مؤشر أداة إنشاء المستندات إليها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// حرك المؤشر إلى حقل MERGEFIELD الأول.
builder.MoveToMergeField("MyMergeField1", true, false);

// لاحظ أن المؤشر يتم وضعه مباشرة بعد حقل الدمج الأول وقبل الثاني.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// إذا أردنا تعديل رمز الحقل أو محتوياته باستخدام المنشئ،
// يجب أن يكون المؤشر داخل الحقل.
// لوضعه داخل حقل، سنحتاج إلى استدعاء أسلوب MoveTo الخاص بمنشئ المستندات
// وتمرير بداية الحقل أو العقدة الفاصلة كوسيطة.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
