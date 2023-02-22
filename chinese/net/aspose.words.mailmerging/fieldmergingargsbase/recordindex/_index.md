---
title: FieldMergingArgsBase.RecordIndex
second_title: Aspose.Words for .NET API 参考
description: FieldMergingArgsBase 财产. 获取正在合并的记录的从零开始的索引
type: docs
weight: 60
url: /zh/net/aspose.words.mailmerging/fieldmergingargsbase/recordindex/
---
## FieldMergingArgsBase.RecordIndex property

获取正在合并的记录的从零开始的索引。

```csharp
public int RecordIndex { get; }
```

### 例子

演示如何在邮件合并期间将复选框表单字段作为合并数据插入 MERGEFIELD。

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 使用带有“TableStart”/“TableEnd”标签的 MERGEFIELD 来定义邮件合并区域
    // 它属于名为“StudentCourse”的数据源，并且有一个 MERGEFIELD，它接受来自名为“CourseName”的列的数据。
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
/// 在遇到具有特定名称的 MERGEFIELD 时，插入复选框表单字段而不是合并数据文本。
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// 当邮件合并将数据合并到 MERGEFIELD 时调用。
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

            // 在这种情况下，对于每个记录索引'n'，对应的字段值为“Course n”。
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // 没做什么。
    }

    private int mCheckBoxCount;
}

/// <summary>
/// 创建邮件合并数据源。
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

### 也可以看看

* class [FieldMergingArgsBase](../)
* 命名空间 [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* 部件 [Aspose.Words](../../../)


