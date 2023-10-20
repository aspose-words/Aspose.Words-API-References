---
title: DocumentProperty Class
linktitle: DocumentProperty
articleTitle: DocumentProperty
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Properties.DocumentProperty 班级. 表示自定义或内置文档属性 在 C#.
type: docs
weight: 4470
url: /zh/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

表示自定义或内置文档属性。

要了解更多信息，请访问[使用文档属性](https://docs.aspose.com/words/net/work-with-document-properties/)文档文章。

```csharp
public class DocumentProperty
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | 显示此属性是否链接到内容。 |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | 获取链接的自定义文档属性的源。 |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | 返回属性的名称。 |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | 获取属性的数据类型。 |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | 获取或设置属性的值。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | 以 bool 形式返回属性值。 |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | 以字节数组形式返回属性值。 |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | 将属性值返回为**约会时间**以 UTC 时间表示。 |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | 以双精度形式返回属性值。 |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | 以整数形式返回属性值。 |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | 以根据当前区域设置格式化的字符串形式返回属性值。 |

## 例子

展示如何使用内置文档属性。

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// “Document”对象在其成员中包含一些元数据。
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// 该文档还将元数据存储在其内置属性中。
// 每个内置属性都是文档的“BuiltInDocumentProperties”对象的成员。
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // 某些属性可能存储多个值。
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

### 也可以看看

* class [DocumentPropertyCollection](../documentpropertycollection/)
* 命名空间 [Aspose.Words.Properties](../../aspose.words.properties/)
* 部件 [Aspose.Words](../../)
