---
title: BaseWebExtensionCollection1.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words for .NET
description: 探索 BaseWebExtensionCollection GetEnumerator 方法，轻松遍历集合，提高开发效率和代码管理。
type: docs
weight: 50
url: /zh/net/aspose.words.webextensions/basewebextensioncollection-1/getenumerator/
---
## BaseWebExtensionCollection&lt;T&gt;.GetEnumerator method

返回一个可以遍历集合的枚举器。

```csharp
public IEnumerator<T> GetEnumerator()
```

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
