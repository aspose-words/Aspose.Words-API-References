---
title: FieldCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 发现 FieldCollection Item 属性，轻松通过索引访问字段并轻松、精确地增强数据管理。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldcollection/item/
---
## FieldCollection indexer

返回指定索引处的字段。

```csharp
public Field this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 集合的索引。 |

## 评论

该索引从零开始。

允许使用负索引，表示从集合的后面进行访问。 例如 -1 表示最后一项，-2 表示倒数第二项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负数并且其绝对值大于列表中的项目数，则返回空引用。

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

* class [Field](../../field/)
* class [FieldCollection](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
