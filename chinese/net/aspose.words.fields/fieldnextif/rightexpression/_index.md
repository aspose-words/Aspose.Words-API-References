---
title: FieldNextIf.RightExpression
second_title: Aspose.Words for .NET API 参考
description: FieldNextIf 财产. 获取或设置比较表达式的右边部分
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldnextif/rightexpression/
---
## FieldNextIf.RightExpression property

获取或设置比较表达式的右边部分。

```csharp
public string RightExpression { get; set; }
```

### 例子

演示如何在邮件合并期间使用 NEXT/NEXTIF 字段将多行合并到一页中。

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 为我们的邮件合并创建一个数据源，包含 3 行。
    // 使用此表的邮件合并通常会创建一个 3 页的文档。
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // 如果我们有多个具有相同 FieldName 的合并字段，
    // 它们会从数据源的同一行接收数据，并在合并后显示相同的值。
    // 一个 NEXT 字段告诉邮件合并立即向下移动一行，
    // 这意味着 NEXT 字段后面的任何 MERGEFIELD 都将从下一行接收数据。
    // 确保不要在已经在最后一行时尝试跳到下一行。
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // 合并后，这些 MERGEFIELD 接受的数据源值
    // 将与上面的 MERGEFIELD 在同一页面上结束。
    InsertMergeFields(builder, "Second row: ");

    // NEXTIF 字段与 NEXT 字段具有相同的功能，
    // 但仅当由以下 3 个属性构造的语句为真时才会跳到下一行。
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // 如果上述字段断言的比较是正确的，
    // 以下 3 个合并字段将从第三行获取数据。
    // 否则，这些字段将再次从第 2 行获取数据。
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // 我们的数据源有 3 行，我们跳过了两次行。
    // 我们的输出文档将有 1 页，其中包含所有 3 行的数据。
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");

/// <summary>
/// 使用文档构建器为包含名为“Courtesy Title”、“First Name”和“Last Name”的列的数据源插入 MERGEFIELD。
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// 使用文档构建器插入具有指定属性的 MERRGEFIELD。
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### 也可以看看

* class [FieldNextIf](../)
* 命名空间 [Aspose.Words.Fields](../../fieldnextif/)
* 部件 [Aspose.Words](../../../)


