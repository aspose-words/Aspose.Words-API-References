---
title: FieldCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: 用于 .NET 的 Aspose.Words
description: FieldCollection Remove 方法. 从此集合和文档中删除指定字段 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.fields/fieldcollection/remove/
---
## FieldCollection.Remove method

从此集合和文档中删除指定字段。

```csharp
public void Remove(Field field)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field | Field | 要删除的字段。 |

## 例子

演示如何从字段集合中删除字段。

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

// 下面是从字段集合中删除字段的四种方法。
// 1 - 获取一个字段来删除自身：
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - 获取集合以删除我们传递给其删除方法的字段：
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - 从索引处的集合中删除字段：
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - 立即从集合中删除所有字段：
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### 也可以看看

* class [Field](../../field/)
* class [FieldCollection](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
