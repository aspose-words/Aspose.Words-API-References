---
title: MailMerge.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: 用于 .NET 的 Aspose.Words
description: MailMerge GetFieldNames 方法. 返回文档中可用的邮件合并字段名称的集合 在 C#.
type: docs
weight: 220
url: /zh/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

返回文档中可用的邮件合并字段名称的集合。

```csharp
public string[] GetFieldNames()
```

## 评论

返回完整的合并字段名称，包括可选前缀。不消除重复的字段名称。

每次调用时都会创建一个新的字符串数组。

包含“mustache”字段名称，如果[`UseNonMergeFields`](../usenonmergefields/)是`真的`。

## 例子

演示如何获取文档中所有合并字段的名称。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Columns.Add("City");
dataTable.Rows.Add(new object[] { "John", "Doe", "New York" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs", "Washington" });

// 对于文档中的每个 MERGEFIELD 名称，确保数据表包含一列
// 同名，然后执行邮件合并。
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
