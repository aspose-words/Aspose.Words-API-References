---
title: FieldMergeField.IsMapped
linktitle: IsMapped
articleTitle: IsMapped
second_title: Aspose.Words for .NET
description: 发现 FieldMergeField IsMapped 属性可以轻松管理映射字段，增强数据集成和工作流效率。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldmergefield/ismapped/
---
## FieldMergeField.IsMapped property

获取或设置此字段是否为映射字段。

```csharp
public bool IsMapped { get; set; }
```

## 例子

展示如何使用 MERGEFIELD 字段执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个数据表作为邮件合并数据源。
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// 插入一个 MERGEFIELD，并将 FieldName 属性设置为数据源中某一列的名称。
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// 合并发生时，我们可以在该字段接受的值之前和之后应用文本。
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());
Assert.AreEqual(FieldType.FieldMergeField, fieldMergeField.Type);

// 在数据源中为不同的列插入另一个 MERGEFIELD。
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### 也可以看看

* class [FieldMergeField](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
