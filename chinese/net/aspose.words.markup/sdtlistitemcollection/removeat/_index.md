---
title: SdtListItemCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words for .NET
description: 使用 SdtListItemCollection RemoveAt 方法，轻松按索引删除列表项。立即简化您的数据管理！
type: docs
weight: 70
url: /zh/net/aspose.words.markup/sdtlistitemcollection/removeat/
---
## SdtListItemCollection.RemoveAt method

删除指定索引处的列表项。

```csharp
public void RemoveAt(int index)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 要删除的项目的从零开始的索引。 |

## 例子

展示如何使用下拉列表结构化文档标签。

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// 下拉列表结构化文档标签是一种允许用户
// 通过左键单击并在 Microsoft Word 中打开表单从列表中选择一个选项。
// “ListItems”属性包含所有列表项，每个列表项都是一个“SdtListItem”。
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// 添加另外 3 个列表项。使用与第一个项不同的构造函数来初始化这些项
// 显示与其值不同的字符串。
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// 下拉列表正在显示第一项。请将其他列表项分配给“SelectedValue”以显示它。
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// 枚举集合并打印每个元素。
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // 删除最后一个列表项。
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// 由于我们的下拉控件默认设置为显示已移除的项目，因此请为其提供一个存在的项目来显示。
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// 使用“Clear”方法一次性清空整个下拉项集合。
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### 也可以看看

* class [SdtListItemCollection](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
