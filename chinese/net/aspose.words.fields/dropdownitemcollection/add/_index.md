---
title: DropDownItemCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: 使用 Add 方法轻松增强您的 DropDownItemCollection。立即添加字符串以扩展您的集合并提升用户体验。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/dropdownitemcollection/add/
---
## DropDownItemCollection.Add method

在集合末尾添加一个字符串。

```csharp
public int Add(string value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | String | 要添加到集合末尾的字符串。 |

### 返回值

插入新元素的从零开始的索引。

## 例子

展示如何插入组合框字段，并编辑其项目集合中的元素。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个组合框，然后验证其下拉项集合。
// 在 Microsoft Word 中，用户将单击组合框，
// 然后选择集合中的一项文本进行显示。
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// 有两种方法可以向现有的下拉框项目集合中添加新项目。
// 1 - 将一个项目附加到集合的末尾：
dropDownItems.Add("Four");

// 2 - 在指定索引处的另一个项目之前插入一个项目：
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// 遍历集合并打印每个元素。
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
