---
title: Document.BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
articleTitle: BuiltInDocumentProperties
second_title: 用于 .NET 的 Aspose.Words
description: Document BuiltInDocumentProperties 财产. 返回一个集合表示文档的所有内置文档属性 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/document/builtindocumentproperties/
---
## Document.BuiltInDocumentProperties property

返回一个集合，表示文档的所有内置文档属性。

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

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

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
