---
title: DocumentBuilder.MoveToMergeField
linktitle: MoveToMergeField
articleTitle: MoveToMergeField
second_title: Aspose.Words لـ .NET
description: تنقل بسهولة بين مستنداتك باستخدام طريقة MoveToMergeField. ضع المؤشر فورًا خارج حقول الدمج لتحرير سلس.
type: docs
weight: 590
url: /ar/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(*string*) {#movetomergefield}

يحرك المؤشر إلى موضع يقع خلف حقل الدمج المحدد ويزيل حقل الدمج.

```csharp
public bool MoveToMergeField(string fieldName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldName | String | اسم حقل دمج البريد غير الحساس لحالة الأحرف. |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على حقل الدمج وتم نقل المؤشر؛`خطأ شنيع` خلاف ذلك.

## ملاحظات

لاحظ أن هذه الطريقة تحذف حقل الدمج من المستند بعد تحريك المؤشر.

## أمثلة

يوضح كيفية ملء حقول MERGEFIELD بالبيانات باستخدام منشئ المستندات بدلاً من دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج بعض MERGEFIELDS، التي تقبل البيانات من الأعمدة التي تحمل نفس الاسم في مصدر البيانات أثناء دمج البريد،
//ثم قم بملئها يدويًا.
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

يوضح كيفية إدراج حقول نموذج مربع الاختيار في MERGEFIELDs كبيانات دمج أثناء دمج البريد.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // استخدم MERGEFIELDs مع علامتي "TableStart"/"TableEnd" لتحديد منطقة دمج البريد
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
/// عند مواجهة MERGEFIELD باسم محدد، يتم إدراج حقل نموذج مربع الاختيار بدلاً من نص بيانات الدمج.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// يتم استدعاؤها عندما يقوم دمج البريد بدمج البيانات في MERGEFIELD.
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

            // في هذه الحالة، لكل فهرس سجل 'n'، قيمة الحقل المقابلة هي "Course n".
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        //لا تفعل شيئا.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// إنشاء مصدر بيانات دمج البريد.
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
| fieldName | String | اسم حقل دمج البريد غير الحساس لحالة الأحرف. |
| isAfter | Boolean | متى`حقيقي` ، يحرك المؤشر ليكون بعد نهاية الحقل. عندما`خطأ شنيع` ، يحرك المؤشر ليكون قبل بداية الحقل. |
| isDeleteField | Boolean | متى`حقيقي`, يحذف حقل الدمج. |

### قيمة الإرجاع

`حقيقي` إذا تم العثور على حقل الدمج وتم نقل المؤشر؛`خطأ شنيع` خلاف ذلك.

## أمثلة

يوضح كيفية إدراج الحقول، ونقل مؤشر منشئ المستندات إليها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// نقل المؤشر إلى MERGEFIELD الأول.
builder.MoveToMergeField("MyMergeField1", true, false);

// لاحظ أن المؤشر يوضع مباشرة بعد MERGEFIELD الأول، وقبل الثاني.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// إذا أردنا تحرير كود الحقل أو محتوياته باستخدام المنشئ،
//يجب أن يكون المؤشر داخل حقل.
// لوضعه داخل حقل، سنحتاج إلى استدعاء طريقة MoveTo الخاصة بمنشئ المستندات
// ومرر عقدة بداية الحقل أو الفاصلة كحجة.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
