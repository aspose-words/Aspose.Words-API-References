---
title: Class BaseWebExtensionCollectionT
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.WebExtensions.BaseWebExtensionCollection1T 班级. 的基类TaskPaneCollectionWebExtensionBindingCollection WebExtensionPropertyCollection和WebExtensionReferenceCollection收藏.
type: docs
weight: 6700
url: /zh/net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

的基类[`TaskPaneCollection`](../taskpanecollection/),[`WebExtensionBindingCollection`](../webextensionbindingcollection/), [`WebExtensionPropertyCollection`](../webextensionpropertycollection/)和[`WebExtensionReferenceCollection`](../webextensionreferencecollection/)收藏.

要了解更多信息，请访问[使用 Office 加载项](https://docs.aspose.com/words/net/work-with-office-add-ins/)文档文章。

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| 范围 | 描述 |
| --- | --- |
| T | 集合项的类型。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } | 获取或设置指定索引处的项目。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(T) | 将指定项目添加到集合中。 |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() | 从集合中删除所有元素。 |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() | 返回一个可以迭代集合的枚举器。 |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(int) | 从集合中删除指定索引处的项目。 |

### 例子

展示如何使用文档的 Web 扩展集合。

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// 打印文档 Web 扩展的所有属性。
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

* 命名空间 [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* 部件 [Aspose.Words](../../)


