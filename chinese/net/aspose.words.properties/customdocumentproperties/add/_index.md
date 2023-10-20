---
title: CustomDocumentProperties.Add
linktitle: Add
articleTitle: Add
second_title: 用于 .NET 的 Aspose.Words
description: CustomDocumentProperties Add 方法. 创建一个新的自定义文档属性String数据类型 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(*string, string*) {#add_4}

创建一个新的自定义文档属性String数据类型.

```csharp
public DocumentProperty Add(string name, string value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| value | String | 财产的价值。 |

### 返回值

新创建的属性对象。

## 例子

展示如何使用文档的自定义属性。

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

// 该集合按字母顺序对自定义属性进行排序。
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

// 我们可以通过“文件”-> 在 Microsoft Word 中找到这些自定义属性“属性”> “高级属性”> “风俗”。
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// 以下是从文档中删除自定义属性的三种方法。
// 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - 立即清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)

---

## Add(*string, int*) {#add_2}

创建一个新的自定义文档属性Number数据类型.

```csharp
public DocumentProperty Add(string name, int value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| value | Int32 | 财产的价值。 |

### 返回值

新创建的属性对象。

## 例子

展示如何使用文档的自定义属性。

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

// 该集合按字母顺序对自定义属性进行排序。
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

// 我们可以通过“文件”-> 在 Microsoft Word 中找到这些自定义属性“属性”> “高级属性”> “风俗”。
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// 以下是从文档中删除自定义属性的三种方法。
// 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - 立即清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)

---

## Add(*string, DateTime*) {#add_3}

创建一个新的自定义文档属性DateTime数据类型.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| value | DateTime | 财产的价值。 |

### 返回值

新创建的属性对象。

## 例子

演示如何创建包含日期和时间的自定义文档属性。

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

展示如何使用文档的自定义属性。

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

// 该集合按字母顺序对自定义属性进行排序。
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

// 我们可以通过“文件”-> 在 Microsoft Word 中找到这些自定义属性“属性”> “高级属性”> “风俗”。
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// 以下是从文档中删除自定义属性的三种方法。
// 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - 立即清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)

---

## Add(*string, bool*) {#add}

创建一个新的自定义文档属性Boolean数据类型.

```csharp
public DocumentProperty Add(string name, bool value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| value | Boolean | 财产的价值。 |

### 返回值

新创建的属性对象。

## 例子

展示如何使用文档的自定义属性。

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

// 该集合按字母顺序对自定义属性进行排序。
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

// 我们可以通过“文件”-> 在 Microsoft Word 中找到这些自定义属性“属性”> “高级属性”> “风俗”。
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// 以下是从文档中删除自定义属性的三种方法。
// 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - 立即清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)

---

## Add(*string, double*) {#add_1}

创建一个新的自定义文档属性Double数据类型.

```csharp
public DocumentProperty Add(string name, double value)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 属性的名称。 |
| value | Double | 财产的价值。 |

### 返回值

新创建的属性对象。

## 例子

展示如何使用文档的自定义属性。

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

// 该集合按字母顺序对自定义属性进行排序。
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

// 我们可以通过“文件”-> 在 Microsoft Word 中找到这些自定义属性“属性”> “高级属性”> “风俗”。
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// 以下是从文档中删除自定义属性的三种方法。
// 1 - 按索引删除：
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - 按名称删除：
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - 立即清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
