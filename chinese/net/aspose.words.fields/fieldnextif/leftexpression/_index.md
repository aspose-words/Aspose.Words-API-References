---
title: FieldNextIf.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words for .NET
description: 探索 FieldNextIf LeftExpression 属性。轻松管理比较表达式的左侧，以增强数据操作和分析能力。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldnextif/leftexpression/
---
## FieldNextIf.LeftExpression property

获取或设置比较表达式的左边部分。

```csharp
public string LeftExpression { get; set; }
```

## 例子

展示如何在邮件合并期间使用 NEXT/NEXTIF 字段将多行合并到一页中。

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 为我们的邮件合并创建一个包含 3 行的数据源。
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
    // 合并后它们将从数据源的同一行接收数据并显示相同的值。
    // NEXT 字段立即指示邮件合并向下移动一行，
    // 这意味着任何跟在 NEXT 字段后面的 MERGEFIELD 都将接收下一行的数据。
    // 确保在最后一行时不要尝试跳到下一行。
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // 合并后，这些 MERGEFIELD 接受的数据源值
    // 将最终出现在与上述 MERGEFIELD 相同的页面上。
    InsertMergeFields(builder, "Second row: ");

    // NEXTIF 字段与 NEXT 字段具有相同的功能，
    // 但仅当由以下 3 个属性构造的语句为真时，它才会跳到下一行。
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
    // 我们的输出文档将有 1 页，包含所有 3 行的数据。
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// 使用文档生成器为包含名为“礼节称谓”、“名字”和“姓氏”的列的数据源插入 MERGEFIELD。
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// 使用文档生成器插入具有指定属性的 MERRGEFIELD。
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
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
