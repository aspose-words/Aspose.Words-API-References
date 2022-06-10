---
title: Add
second_title: Aspose.Words for .NET API 参考
description: 创建 PropertyType.String 的新自定义文档属性数据类型
type: docs
weight: 10
url: /zh/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(string, string) {#add_4}

创建 **PropertyType.String** 的新自定义文档属性数据类型。

```csharp
public DocumentProperty Add(string name, string value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| value | String | 属性的值。 |

### 返回值

新创建的属性对象。

### 例子

显示如何使用文档的自定义属性。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

 // 自定义文档属性是我们可以添加到文档中的键值对。
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

 // 集合按字母顺序对自定义属性进行排序。
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

 // 打印文档中的每个自定义属性。
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

 // 使用 DOCPROPERTY 字段显示自定义属性的值。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

 // 我们可以通过“文件”在 Microsoft Word 中找到这些自定义属性 -> “属性” > “高级属性”> “自定义”.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

 // 下面是三种方法或从文档中删除自定义属性。
 // 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

 // 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

 // 3 - 一次清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* 命名空间 [Aspose.Words.Properties](../../customdocumentproperties)
* 部件 [Aspose.Words](../../../)

---

## Add(string, int) {#add_2}

创建 **PropertyType.Number** 数据类型的新自定义文档属性。

```csharp
public DocumentProperty Add(string name, int value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| value | Int32 | 属性的值。 |

### 返回值

新创建的属性对象。

### 例子

显示如何使用文档的自定义属性。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

 // 自定义文档属性是我们可以添加到文档中的键值对。
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

 // 集合按字母顺序对自定义属性进行排序。
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

 // 打印文档中的每个自定义属性。
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

 // 使用 DOCPROPERTY 字段显示自定义属性的值。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

 // 我们可以通过“文件”在 Microsoft Word 中找到这些自定义属性 -> “属性” > “高级属性”> “自定义”.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

 // 下面是三种方法或从文档中删除自定义属性。
 // 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

 // 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

 // 3 - 一次清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* 命名空间 [Aspose.Words.Properties](../../customdocumentproperties)
* 部件 [Aspose.Words](../../../)

---

## Add(string, DateTime) {#add_3}

创建 **PropertyType.DateTime** 数据类型的新自定义文档属性。

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| value | DateTime | 属性的值。 |

### 返回值

新创建的属性对象。

### 例子

展示如何创建包含日期和时间的自定义文档属性。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

 // 自定义文档属性是我们可以添加到文档中的键值对。
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

 // 集合按字母顺序对自定义属性进行排序。
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

 // 打印文档中的每个自定义属性。
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

 // 使用 DOCPROPERTY 字段显示自定义属性的值。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

 // 我们可以通过“文件”在 Microsoft Word 中找到这些自定义属性 -> “属性” > “高级属性”> “自定义”.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

 // 下面是三种方法或从文档中删除自定义属性。
 // 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

 // 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

 // 3 - 一次清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

显示如何使用文档的自定义属性。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

 // 自定义文档属性是我们可以添加到文档中的键值对。
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

 // 集合按字母顺序对自定义属性进行排序。
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

 // 打印文档中的每个自定义属性。
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

 // 使用 DOCPROPERTY 字段显示自定义属性的值。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

 // 我们可以通过“文件”在 Microsoft Word 中找到这些自定义属性 -> “属性” > “高级属性”> “自定义”.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

 // 下面是三种方法或从文档中删除自定义属性。
 // 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

 // 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

 // 3 - 一次清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* 命名空间 [Aspose.Words.Properties](../../customdocumentproperties)
* 部件 [Aspose.Words](../../../)

---

## Add(string, bool) {#add}

创建 **PropertyType.Boolean** 数据类型的新自定义文档属性。

```csharp
public DocumentProperty Add(string name, bool value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| value | Boolean | 属性的值。 |

### 返回值

新创建的属性对象。

### 例子

显示如何使用文档的自定义属性。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

 // 自定义文档属性是我们可以添加到文档中的键值对。
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

 // 集合按字母顺序对自定义属性进行排序。
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

 // 打印文档中的每个自定义属性。
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

 // 使用 DOCPROPERTY 字段显示自定义属性的值。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

 // 我们可以通过“文件”在 Microsoft Word 中找到这些自定义属性 -> “属性” > “高级属性”> “自定义”.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

 // 下面是三种方法或从文档中删除自定义属性。
 // 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

 // 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

 // 3 - 一次清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* 命名空间 [Aspose.Words.Properties](../../customdocumentproperties)
* 部件 [Aspose.Words](../../../)

---

## Add(string, double) {#add_1}

创建 **PropertyType.Float** 数据类型的新自定义文档属性。

```csharp
public DocumentProperty Add(string name, double value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| value | Double | 属性的值。 |

### 返回值

新创建的属性对象。

### 例子

显示如何使用文档的自定义属性。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

 // 自定义文档属性是我们可以添加到文档中的键值对。
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

 // 集合按字母顺序对自定义属性进行排序。
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

 // 打印文档中的每个自定义属性。
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

 // 使用 DOCPROPERTY 字段显示自定义属性的值。
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

 // 我们可以通过“文件”在 Microsoft Word 中找到这些自定义属性 -> “属性” > “高级属性”> “自定义”.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

 // 下面是三种方法或从文档中删除自定义属性。
 // 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

 // 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

 // 3 - 一次清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../../documentproperty)
* class [CustomDocumentProperties](../../customdocumentproperties)
* 命名空间 [Aspose.Words.Properties](../../customdocumentproperties)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
