---
title: MoveToMergeField
second_title: Aspose.Words لمراجع .NET API
description: ينقل المؤشر إلى موضع خارج حقل الدمج المحدد ويزيل حقل الدمج.
type: docs
weight: 530
url: /ar/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(string) {#movetomergefield}

ينقل المؤشر إلى موضع خارج حقل الدمج المحدد ويزيل حقل الدمج.

```csharp
public bool MoveToMergeField(string fieldName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldName | String | الاسم غير المتحسس لحالة الأحرف لحقل دمج المراسلات. |

### قيمة الإرجاع

صحيح إذا تم العثور على حقل الدمج وتم نقل المؤشر ؛ خطأ خلاف ذلك.

### ملاحظات

لاحظ أن هذه الطريقة تحذف حقل الدمج من المستند بعد تحريك المؤشر.

### أمثلة

يوضح كيفية تعبئة MERGEFIELD بالبيانات باستخدام أداة إنشاء المستندات بدلاً من دمج المراسلات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل بعض MERGEFIELDS ، التي تقبل البيانات من أعمدة تحمل الاسم نفسه في مصدر بيانات أثناء دمج البريد ،
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

يوضح كيفية إدراج حقول نموذج مربع الاختيار في MERGEFIELDs كبيانات دمج أثناء دمج البريد.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // استخدم MERGEFIELDs مع علامات "TableStart" / "TableEnd" لتعريف منطقة دمج المراسلات
    // الذي ينتمي إلى مصدر بيانات يسمى "StudentCourse" ولديه MERGEFIELD الذي يقبل البيانات من عمود يسمى "CourseName".
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

/// <summary>
/// عند مواجهة MERGEFIELD باسم معين ، يقوم بإدراج حقل نموذج خانة اختيار بدلاً من دمج نص البيانات.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// يتم الاستدعاء عندما يقوم دمج المراسلات بدمج البيانات في MERGEFIELD.
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

            // في هذه الحالة ، لكل فهرس سجل 'n' قيمة الحقل المقابلة هي "Course n".
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
/// ينشئ مصدر بيانات لدمج المراسلات.
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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## MoveToMergeField(string, bool, bool) {#movetomergefield_1}

نقل حقل الدمج إلى حقل الدمج المحدد.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fieldName | String | الاسم غير المتحسس لحالة الأحرف لحقل دمج المراسلات. |
| isAfter | Boolean | عندما يكون صحيحًا ، ينقل المؤشر ليكون بعد نهاية الحقل . عندما يكون خطأ ، ينقل المؤشر ليكون قبل بدء الحقل. |
| isDeleteField | Boolean | عندما يكون صحيحًا ، يحذف حقل الدمج. |

### قيمة الإرجاع

صحيح إذا تم العثور على حقل الدمج وتم نقل المؤشر ؛ خطأ خلاف ذلك.

### أمثلة

يوضح كيفية إدراج الحقول ، وتحريك مؤشر منشئ المستندات إليها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// حرك المؤشر إلى MERGEFIELD الأول.
builder.MoveToMergeField("MyMergeField1", true, false);

// لاحظ أن المؤشر يتم وضعه مباشرة بعد MERGEFIELD الأول وقبل الثاني.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// إذا كنا نرغب في تحرير رمز الحقل أو المحتويات باستخدام المنشئ ،
// يجب أن يكون مؤشرها داخل حقل.
// لوضعه داخل حقل ، سنحتاج إلى استدعاء طريقة MoveTo لمنشئ المستندات
// وتمرير بداية الحقل أو العقدة الفاصلة كوسيطة.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
