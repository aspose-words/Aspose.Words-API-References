---
title: Class DocumentProperty
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Properties.DocumentProperty 班级. 表示自定义或内置文档属性
type: docs
weight: 4220
url: /zh/net/aspose.words.properties/documentproperty/
---
## DocumentProperty class

表示自定义或内置文档属性。

```csharp
public class DocumentProperty
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [IsLinkToContent](../../aspose.words.properties/documentproperty/islinktocontent/) { get; } | 显示此属性是否链接到内容。 |
| [LinkSource](../../aspose.words.properties/documentproperty/linksource/) { get; } | 获取链接的自定义文档属性的来源。 |
| [Name](../../aspose.words.properties/documentproperty/name/) { get; } | 返回属性的名称。 |
| [Type](../../aspose.words.properties/documentproperty/type/) { get; } | 获取属性的数据类型。 |
| [Value](../../aspose.words.properties/documentproperty/value/) { get; set; } | 获取或设置属性的值。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ToBool](../../aspose.words.properties/documentproperty/tobool/)() | 将属性值返回为布尔值。 |
| [ToByteArray](../../aspose.words.properties/documentproperty/tobytearray/)() | 以字节数组的形式返回属性值。 |
| [ToDateTime](../../aspose.words.properties/documentproperty/todatetime/)() | 以 UTC 格式将属性值返回为 DateTime。 |
| [ToDouble](../../aspose.words.properties/documentproperty/todouble/)() | 以 double 形式返回属性值。 |
| [ToInt](../../aspose.words.properties/documentproperty/toint/)() | 以整数形式返回属性值。 |
| override [ToString](../../aspose.words.properties/documentproperty/tostring/)() | 以根据当前语言环境格式化的字符串形式返回属性值。 |

### 例子

显示如何使用内置文档属性。

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// “文档”对象在其成员中包含一些元数据。
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// 文档还在其内置属性中存储元数据。
// 每个内置属性都是文档“BuiltInDocumentProperties”对象的成员。
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


