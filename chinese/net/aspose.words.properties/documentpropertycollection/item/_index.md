---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: 用于 .NET 的 Aspose.Words
description: DocumentPropertyCollection Item 财产. 返回一个DocumentProperty按属性名称的对象 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

返回一个[`DocumentProperty`](../../documentproperty/)按属性名称的对象。

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| 范围 | 描述 |
| --- | --- |
| name | 要检索的属性的不区分大小写的名称。 |

## 评论

如果未找到具有指定名称的属性，则返回 null。

## 例子

演示如何创建包含日期和时间的自定义文档属性。

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

### 也可以看看

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

返回一个[`DocumentProperty`](../../documentproperty/)按索引的对象.

```csharp
public DocumentProperty this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 的从零开始的索引[`DocumentProperty`](../../documentproperty/)检索。 |

## 例子

显示如何使用自定义文档属性。

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// 每个文档都包含一个自定义属性的集合，这些属性和内置属性一样，是键值对。
// 文档有一个固定的内置属性列表。用户创建所有自定义属性。 
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### 也可以看看

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
