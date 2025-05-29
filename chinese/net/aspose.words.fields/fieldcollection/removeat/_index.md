---
title: FieldCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words for .NET
description: 使用 FieldCollection RemoveAt 方法轻松从文档中移除字段。立即简化您的数据管理！
type: docs
weight: 60
url: /zh/net/aspose.words.fields/fieldcollection/removeat/
---
## FieldCollection.RemoveAt method

从此集合和文档中删除指定索引处的字段。

```csharp
public void RemoveAt(int index)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 集合的索引。 |

## 例子

展示如何从字段集合中删除字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// 以下是从字段集合中删除字段的四种方法。
// 1 - 获取要删除的字段：
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - 获取要删除的字段的集合，并将其传递给其删除方法：
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - 从集合中移除索引处的字段：
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - 一次性从集合中删除所有字段：
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### 也可以看看

* class [FieldCollection](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
