---
title: DocumentPropertyCollection.Count
linktitle: Count
articleTitle: Count
second_title: 用于 .NET 的 Aspose.Words
description: DocumentPropertyCollection Count 财产. 获取集合中的项目数 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.properties/documentpropertycollection/count/
---
## DocumentPropertyCollection.Count property

获取集合中的项目数。

```csharp
public int Count { get; }
```

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

* class [DocumentPropertyCollection](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
