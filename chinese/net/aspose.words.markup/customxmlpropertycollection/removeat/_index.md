---
title: CustomXmlPropertyCollection.RemoveAt
second_title: Aspose.Words for .NET API 参考
description: CustomXmlPropertyCollection 方法. 删除指定索引处的属性
type: docs
weight: 90
url: /zh/net/aspose.words.markup/customxmlpropertycollection/removeat/
---
## CustomXmlPropertyCollection.RemoveAt method

删除指定索引处的属性。

```csharp
public void RemoveAt(int index)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 从零开始的索引。 |

### 例子

展示如何使用智能标记属性来获取有关智能标记的深入信息。

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// 智能标签出现在 Microsoft Word 文档中，将其文本的一部分识别为某种形式的数据，
// 例如名称、日期或地址，并将其转换为显示紫色点状下划线的超链接。
// 在Word 2003中，我们可以通过“工具”->启用智能标签“自动更正选项...”-> “智能标签”。
// 在我们的输入文档中，Microsoft Word 注册了三个对象作为智能标记。
// 智能标签可以嵌套，因此这个集合包含更多。
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// 智能标记的“Properties”成员包含其元数据，每种类型的智能标记的元数据都不同。
// “日期”类型智能标签的属性包含其年、月、日。
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

// 下面是从属性集合中删除元素的三种方法。
// 1 - 按索引删除：
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - 按名称删除：
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - 立即清除整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [CustomXmlPropertyCollection](../)
* 命名空间 [Aspose.Words.Markup](../../customxmlpropertycollection/)
* 部件 [Aspose.Words](../../../)


