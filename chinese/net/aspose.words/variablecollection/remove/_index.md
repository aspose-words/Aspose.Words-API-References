---
title: VariableCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: 使用 VariableCollection Remove 方法轻松删除文档变量。此高效解决方案简化您的数据管理。
type: docs
weight: 80
url: /zh/net/aspose.words/variablecollection/remove/
---
## VariableCollection.Remove method

从集合中删除具有指定名称的文档变量。

```csharp
public void Remove(string name)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 变量的名称不区分大小写。 |

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

* class [VariableCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
