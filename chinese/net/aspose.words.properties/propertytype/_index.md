---
title: PropertyType Enum
linktitle: PropertyType
articleTitle: PropertyType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PropertyType 枚举，轻松定义文档属性数据类型，以增强文档管理和定制。
type: docs
weight: 5230
url: /zh/net/aspose.words.properties/propertytype/
---
## PropertyType enumeration

指定文档属性的数据类型。

```csharp
public enum PropertyType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Boolean | `0` | 该属性是一个布尔值。 |
| DateTime | `1` | 该属性是日期时间值。 |
| Double | `2` | 该属性是一个浮点数。 |
| Number | `3` | 该属性是一个整数。 |
| String | `4` | 该属性是一个字符串值。 |
| StringArray | `5` | 该属性是一个字符串数组。 |
| ObjectArray | `6` | 该属性是一个对象数组。 |
| ByteArray | `7` | 该属性是一个字节数组。 |
| Other | `8` | 该属性是其他类型。 |

## 例子

展示如何使用文档的自定义属性。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// 自定义文档属性是我们可以添加到文档的键值对。
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

// 我们可以在 Microsoft Word 中通过“文件”->“属性”->“高级属性”->“自定义”找到这些自定义属性。
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

// 3 - 一次清空整个集合：
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### 也可以看看

* class [DocumentProperty](../documentproperty/)
* property [Type](../documentproperty/type/)
* 命名空间 [Aspose.Words.Properties](../../aspose.words.properties/)
* 部件 [Aspose.Words](../../)
