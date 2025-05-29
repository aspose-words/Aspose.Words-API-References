---
title: CustomXmlProperty.Uri
linktitle: Uri
articleTitle: Uri
second_title: Aspose.Words for .NET
description: 使用 CustomXmlProperty Uri 轻松管理您的自定义 XML 属性。轻松设置或检索命名空间 URI，以增强功能。
type: docs
weight: 30
url: /zh/net/aspose.words.markup/customxmlproperty/uri/
---
## CustomXmlProperty.Uri property

获取或设置自定义 XML 属性或智能标记属性的命名空间 URI。

```csharp
public string Uri { get; set; }
```

## 评论

不可能`无效的`。

默认为空字符串。

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

* class [CustomXmlProperty](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
