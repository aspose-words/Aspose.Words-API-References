---
title: DocumentProperty.ToString
linktitle: ToString
articleTitle: ToString
second_title: 用于 .NET 的 Aspose.Words
description: DocumentProperty ToString 方法. 以根据当前语言环境格式化的字符串形式返回属性值 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty.ToString method

以根据当前语言环境格式化的字符串形式返回属性值。

```csharp
public override string ToString()
```

## 评论

将布尔属性转换为“Y”或“N”。 将日期属性转换为短日期字符串。 对于所有其他类型，使用 Object.ToString() 转换属性。

## 例子

显示自定义文档属性的各种类型转换方法。

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

显示如何使用自定义文档属性。

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// 每个文档都包含一个自定义属性的集合，这些属性和内置属性一样，是键值对。
// 文档有一个固定的内置属性列表。用户创建所有自定义属性。 
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### 也可以看看

* class [DocumentProperty](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
