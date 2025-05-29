---
title: FieldMergingArgsBase.FieldName
linktitle: FieldName
articleTitle: FieldName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldName في FieldMergingArgsBase، التي تسترد اسم حقل الدمج من مصدر البيانات لديك لتحقيق تكامل سلس.
type: docs
weight: 40
url: /ar/net/aspose.words.mailmerging/fieldmergingargsbase/fieldname/
---
## FieldMergingArgsBase.FieldName property

يحصل على اسم حقل الدمج في مصدر البيانات.

```csharp
public string FieldName { get; }
```

## ملاحظات

إذا كان لديك تعيين من اسم حقل مستند إلى اسم حقل مصدر بيانات مختلف، ، فهذا هو اسم الحقل المعيّن.

إذا قمت بتحديد بادئة اسم الحقل، على سبيل المثال "Image:MyFieldName" في المستند، ثم`FieldName` يقوم بإرجاع اسم الحقل بدون البادئة، أي "MyFieldName".

## أمثلة

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

* class [FieldMergingArgsBase](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
