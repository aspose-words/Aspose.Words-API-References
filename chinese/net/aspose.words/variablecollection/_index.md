---
title: VariableCollection Class
linktitle: VariableCollection
articleTitle: VariableCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.VariableCollection，有效管理和定制文档变量，以增强文档自动化和灵活性。
type: docs
weight: 7380
url: /zh/net/aspose.words/variablecollection/
---
## VariableCollection class

文档变量的集合。

要了解更多信息，请访问[使用文档属性](https://docs.aspose.com/words/net/work-with-document-properties/)文档文章。

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | 通过不区分大小写的名称获取或设置文档变量。 `无效的`值不允许作为赋值的右侧，并将被替换为空字符串。 (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(*string, string*) | 将文档变量添加到集合中。 |
| [Clear](../../aspose.words/variablecollection/clear/)() | 从集合中删除所有元素。 |
| [Contains](../../aspose.words/variablecollection/contains/)(*string*) | 确定集合是否包含具有给定名称的文档变量。 |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有变量。 |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(*string*) | 返回集合中指定文档变量的从零开始的索引。 |
| [Remove](../../aspose.words/variablecollection/remove/)(*string*) | 从集合中删除具有指定名称的文档变量。 |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(*int*) | 删除指定索引处的文档变量。 |

## 评论

变量名称和值都是字符串。

变量名不区分大小写。

## 例子

展示如何使用文档的变量集合。

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// 每个文档都有一个键/值对变量的集合，我们可以向其中添加项目。
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// 我们可以使用 DOCVARIABLE 字段在文档正文中显示变量的值。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// 为现有键分配值将会更新它们。
variables.Add("Home address", "456 Queen St.");

// 然后我们必须更新 DOCVARIABLE 字段以确保它们显示最新值。
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// 验证具有特定名称或值的文档变量是否存在。
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// 变量集合自动按名称的字母顺序对变量进行排序。
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

// 枚举变量集合。
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// 以下是从集合中删除文档变量的三种方法。
// 1 - 按名称：
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - 按索引：
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - 一次清除整个集合：
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
