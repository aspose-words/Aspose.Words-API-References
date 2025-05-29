---
title: MailMerge.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words for .NET
description: 发现 MailMerge GetFieldNames 方法可以轻松访问和利用文档中的所有邮件合并字段名称，从而简化文档自动化。
type: docs
weight: 220
url: /zh/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

返回文档中可用的邮件合并字段名称集合。

```csharp
public string[] GetFieldNames()
```

## 评论

返回包含可选前缀的完整合并字段名称。不会消除重复的字段名称。

每次调用时都会创建一个新的字符串数组。

如果包含“胡子”字段名称[`UseNonMergeFields`](../usenonmergefields/)是`真的`。

## 例子

展示如何获取文档中所有合并字段的名称。

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
// 具有相同的名称，然后执行邮件合并。
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
