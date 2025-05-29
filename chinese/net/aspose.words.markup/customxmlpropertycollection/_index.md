---
title: CustomXmlPropertyCollection Class
linktitle: CustomXmlPropertyCollection
articleTitle: CustomXmlPropertyCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.CustomXmlPropertyCollection，一个用于有效管理自定义 XML 属性和智能标签属性的强大工具。
type: docs
weight: 4640
url: /zh/net/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class

表示自定义 XML 属性或智能标记属性的集合。

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class CustomXmlPropertyCollection : IEnumerable<CustomXmlProperty>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpropertycollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words.markup/customxmlpropertycollection/item/) { get; } | 获取具有指定名称的属性。 (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpropertycollection/add/)(*[CustomXmlProperty](../customxmlproperty/)*) | 向集合添加属性。 |
| [Clear](../../aspose.words.markup/customxmlpropertycollection/clear/)() | 从集合中删除所有元素。 |
| [Contains](../../aspose.words.markup/customxmlpropertycollection/contains/)(*string*) | 确定集合是否包含具有给定名称的属性。 |
| [GetEnumerator](../../aspose.words.markup/customxmlpropertycollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [IndexOfKey](../../aspose.words.markup/customxmlpropertycollection/indexofkey/)(*string*) | 返回集合中指定属性的从零开始的索引。 |
| [Remove](../../aspose.words.markup/customxmlpropertycollection/remove/)(*string*) | 从集合中删除具有指定名称的属性。 |
| [RemoveAt](../../aspose.words.markup/customxmlpropertycollection/removeat/)(*int*) | 删除指定索引处的属性。 |

## 评论

项目是[`CustomXmlProperty`](../customxmlproperty/)对象。

## 例子

展示如何使用智能标记属性来获取有关智能标记的深入信息。

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// 智能标签出现在 Microsoft Word 的文档中，它将其部分文本识别为某种形式的数据，
// 例如姓名、日期或地址，并将其转换为显示紫色虚线下划线的超链接。
// 在 Word 2003 中，我们可以通过“工具”->“自动更正选项...”->“智能标记”来启用智能标记。
// 在我们的输入文档中，有三个 Microsoft Word 注册为智能标记的对象。
// 智能标签可以嵌套，因此该集合包含更多。
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// 智能标签的“属性”成员包含其元数据，每种类型的智能标签的元数据都不同。
// “日期”类型智能标签的属性包含年、月、日。
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// 我们还可以通过各种方式访问属性，例如键值对。
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// 以下是从属性集合中删除元素的三种方法。
// 1 - 按索引删除：
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - 按名称删除：
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - 一次清除整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [CustomXmlProperty](../customxmlproperty/)
* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
