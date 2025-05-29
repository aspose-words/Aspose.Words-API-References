---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 使用我们的 DocumentPropertyCollection 项轻松访问 DocumentProperty 对象。按名称检索属性，实现无缝文档管理。
type: docs
weight: 20
url: /zh/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

返回[`DocumentProperty`](../../documentproperty/)对象通过属性名称.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| 范围 | 描述 |
| --- | --- |
| name | 要检索的属性的名称（不区分大小写）。 |

## 评论

返回`无效的`如果未找到具有指定名称的属性。

## 例子

展示如何创建包含日期和时间的自定义文档属性。

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

### 也可以看看

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

返回[`DocumentProperty`](../../documentproperty/)按索引排序的对象.

```csharp
public DocumentProperty this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 从零开始的索引[`DocumentProperty`](../../documentproperty/)检索。 |

## 例子

展示如何使用自定义文档属性。

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// 每个文档都包含一个自定义属性集合，这些属性与内置属性一样，都是键值对。
 // 文档具有固定的内置属性列表。用户创建所有自定义属性。
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
