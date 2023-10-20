---
title: VariableCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: 用于 .NET 的 Aspose.Words
description: VariableCollection Contains 方法. 确定集合中是否包含具有给定名称的文档变量 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words/variablecollection/contains/
---
## VariableCollection.Contains method

确定集合中是否包含具有给定名称的文档变量。

```csharp
public bool Contains(string name)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 要查找的文档变量的名称（不区分大小写）。 |

### 返回值

`真的`如果在集合中找到项目；否则，`错误的`。

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

// 为现有键分配值将更新它们。
variables.Add("Home address", "456 Queen St.");

// 然后我们必须更新 DOCVARIABLE 字段以确保它们显示最新值。
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// 验证具有特定名称或值的文档变量是否存在。
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// 变量集合自动按名称字母顺序对变量进行排序。
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

// 枚举变量集合。
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// 下面是从集合中删除文档变量的三种方法。
// 1 - 按名称：
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - 按索引：
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - 立即清除整个集合：
variables.Clear();

Assert.That(variables, Is.Empty);
```

### 也可以看看

* class [VariableCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
