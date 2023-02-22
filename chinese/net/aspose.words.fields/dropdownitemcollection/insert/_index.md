---
title: DropDownItemCollection.Insert
second_title: Aspose.Words for .NET API 参考
description: DropDownItemCollection 方法. 将字符串插入到集合中指定索引处
type: docs
weight: 80
url: /zh/net/aspose.words.fields/dropdownitemcollection/insert/
---
## DropDownItemCollection.Insert method

将字符串插入到集合中指定索引处。

```csharp
public void Insert(int index, string value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 插入值的从零开始的索引。 |
| value | String | 要插入的字符串。 |

### 例子

演示如何插入组合框字段，并编辑其项目集合中的元素。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个组合框，然后验证它的下拉项集合。
// 在 Microsoft Word 中，用户将单击组合框，
// 然后选择要显示的集合中的文本项之一。
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
* 命名空间 [Aspose.Words.Fields](../../dropdownitemcollection/)
* 部件 [Aspose.Words](../../../)


