---
title: DropDownItemCollection Class
linktitle: DropDownItemCollection
articleTitle: DropDownItemCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.DropDownItemCollection 类 - 轻松管理表单字段中的下拉项的解决方案！
type: docs
weight: 1910
url: /zh/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

表示下拉表单字段中所有项目的字符串集合。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | 获取或设置指定索引处的元素。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(*string*) | 在集合末尾添加一个字符串。 |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | 从集合中删除所有元素。 |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(*string*) | 确定集合是否包含指定的值。 |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(*string*) | 返回集合中指定值的从零开始的索引。 |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(*int, string*) | 将字符串插入到指定索引处的集合中。 |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(*string*) | 从集合中删除指定的值。 |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(*int*) | 删除指定索引处的值。 |

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

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
