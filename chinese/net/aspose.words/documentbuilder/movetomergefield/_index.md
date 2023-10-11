---
title: DocumentBuilder.MoveToMergeField
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 将光标移动到指定合并字段之外的位置并删除合并字段
type: docs
weight: 560
url: /zh/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(string) {#movetomergefield}

将光标移动到指定合并字段之外的位置并删除合并字段。

```csharp
public bool MoveToMergeField(string fieldName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldName | String | 邮件合并字段的名称（不区分大小写）。 |

### 返回值

`真的`如果找到合并字段并且光标已移动；`错误的`否则。

### 评论

请注意，此方法会在移动光标后从文档中删除合并字段。

### 例子

演示如何使用文档生成器而不是邮件合并来填充数据MERGEFIELD。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一些 MERGEFIELDS，它们在邮件合并期间接受数据源中同名列的数据，
// 然后手动填充它们。
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

演示如何在邮件合并期间将复选框表单字段作为合并数据插入到 MERGEFIELD 中。

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 使用带有“TableStart”/“TableEnd”标记的 MERGEFIELD 来定义邮件合并区域
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
}

/// <summary>
/// 遇到具有特定名称的 MERGEFIELD 时，插入复选框表单字段而不是合并数据文本。
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

            // 在这种情况下，对于每个记录索引'n'，对应的字段值为“课程n”。
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

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## MoveToMergeField(string, bool, bool) {#movetomergefield_1}

将合并字段移动到指定的合并字段。

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldName | String | 邮件合并字段的名称（不区分大小写）。 |
| isAfter | Boolean | 什么时候`真的` , 将光标移动到字段末尾之后。 时`错误的`，将光标移动到字段开始之前。 |
| isDeleteField | Boolean | 什么时候`真的`，删除合并字段。 |

### 返回值

`真的`如果找到合并字段并且光标已移动；`错误的`否则。

### 例子

演示如何插入字段，以及如何将文档生成器的光标移至这些字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// 将光标移动到第一个 MERGEFIELD。
builder.MoveToMergeField("MyMergeField1", true, false);

// 请注意，光标紧邻第一个 MERGEFIELD 之后和第二个 MERGEFIELD 之前。
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// 如果我们希望使用构建器编辑字段的字段代码或内容，
// 它的光标需要位于字段内。
// 要将其放置在字段中，我们需要调用文档构建器的 MoveTo 方法
// 并将字段的开始或分隔符节点作为参数传递。
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


