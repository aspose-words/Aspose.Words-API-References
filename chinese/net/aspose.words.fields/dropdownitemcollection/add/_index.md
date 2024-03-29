---
title: DropDownItemCollection.Add
linktitle: Add
articleTitle: Add
second_title: 用于 .NET 的 Aspose.Words
description: DropDownItemCollection Add 方法. 将字符串添加到集合的末尾 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.fields/dropdownitemcollection/add/
---
## DropDownItemCollection.Add method

将字符串添加到集合的末尾。

```csharp
public int Add(string value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | String | 要添加到集合末尾的字符串。 |

### 返回值

插入新元素的从零开始的索引。

## 例子

演示如何插入组合框字段以及编辑其项目集合中的元素。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个组合框，然后验证其下拉项集合。
// 在 Microsoft Word 中，用户将单击组合框，
// 然后选择集合中要显示的文本项之一。
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// 有两种方法可以将新项目添加到现有的下拉框项目集合中。
// 1 - 将一个项目附加到集合的末尾：
dropDownItems.Add("Four");

// 2 - 在指定索引处的另一个项目之前插入一个项目：
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// 迭代集合并打印每个元素。
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// 有两种方法可以从下拉项集合中删除元素。
// 1 - 删除内容等于传递的字符串的项目：
dropDownItems.Remove("Four");

// 2 - 删除索引处的项目：
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// 清空整个下拉项集合。
dropDownItems.Clear();
```

### 也可以看看

* class [DropDownItemCollection](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
