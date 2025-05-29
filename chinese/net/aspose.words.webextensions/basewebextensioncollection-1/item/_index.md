---
title: BaseWebExtensionCollection1.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 探索 BaseWebExtensionCollection 的 Item 属性，轻松按索引管理项目。立即使用高效的数据处理简化您的开发！
type: docs
weight: 20
url: /zh/net/aspose.words.webextensions/basewebextensioncollection-1/item/
---
## BaseWebExtensionCollection&lt;T&gt; indexer

获取或设置指定索引处的项目。

```csharp
public T this[int index] { get; set; }
```

| 范围 | 描述 |
| --- | --- |
| index | 该项目的从零开始的索引。 |

## 例子

展示如何使用文档的 Web 扩展集合。

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// 打印文档的 Web 扩展的所有属性。
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// 删除网络扩展。
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### 也可以看看

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* 命名空间 [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* 部件 [Aspose.Words](../../../)
