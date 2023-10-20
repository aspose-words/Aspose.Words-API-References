---
title: CustomXmlPropertyCollection.Add
linktitle: Add
articleTitle: Add
second_title: 用于 .NET 的 Aspose.Words
description: CustomXmlPropertyCollection Add 方法. 将属性添加到集合中 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.markup/customxmlpropertycollection/add/
---
## CustomXmlPropertyCollection.Add method

将属性添加到集合中。

```csharp
public void Add(CustomXmlProperty property)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| property | CustomXmlProperty | 要添加的属性。 |

## 例子

展示如何使用智能标签属性来获取有关智能标签的深入信息。

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// 智能标记出现在文档中，Microsoft Word 将其文本的一部分识别为某种形式的数据，
// 例如姓名、日期或地址，并将其转换为显示紫色虚线下划线的超链接。
// 在 Word 2003 中，我们可以通过“工具”启用智能标签 -> “自动更正选项...” -> “智能标签”。
// 在我们的输入文档中，Microsoft Word 将三个对象注册为智能标记。
// 智能标签可能是嵌套的，所以这个集合包含更多。
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// 智能标签的“属性”成员包含其元数据，对于每种类型的智能标签，元数据会有所不同。
// “日期”类型智能标签的属性包含它的年、月和日。
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

// 下面是从属性集合中移除元素的三种方法。
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

* class [CustomXmlProperty](../../customxmlproperty/)
* class [CustomXmlPropertyCollection](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
