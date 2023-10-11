---
title: Class SdtListItemCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Markup.SdtListItemCollection 班级. 提供对SdtListItem结构化文档标签的元素
type: docs
weight: 4030
url: /zh/net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

提供对[`SdtListItem`](../sdtlistitem/)结构化文档标签的元素。

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | 获取集合中的项目数。 |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | 返回一个[`SdtListItem`](../sdtlistitem/)对象在集合中给出从零开始的索引。 |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | 指定此列表中当前选定的值。 允许空值，这意味着当前选定的条目没有与此列表项集合关联。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(SdtListItem) | 将项目添加到此集合。 |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | 清除此集合中的所有项目。 |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(int) | 删除指定索引处的列表项。 |

### 例子

展示如何使用下拉列表结构化文档标签。

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// 下拉列表结构化文档标签是一种允许用户
// 通过左键单击并在 Microsoft Word 中打开表单，从列表中选择一个选项。
// “ListItems”属性包含所有列表项，每个列表项都是一个“SdtListItem”。
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// 添加 3 个列表项。使用与第一项不同的构造函数来初始化这些项
// 显示与其值不同的字符串。
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// 下拉列表显示第一项。将不同的列表项分配给“SelectedValue”以显示它。
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

// 由于我们的下拉控件默认设置为显示已删除的项目，因此给它一个要显示存在的项目。
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// 使用“Clear”方法一次性清空整个下拉项集合。
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### 也可以看看

* class [SdtListItem](../sdtlistitem/)
* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)


