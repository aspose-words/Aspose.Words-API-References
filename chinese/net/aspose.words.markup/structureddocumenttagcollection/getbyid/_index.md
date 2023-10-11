---
title: StructuredDocumentTagCollection.GetById
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTagCollection 方法. 按标识符返回结构化文档标签
type: docs
weight: 30
url: /zh/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

按标识符返回结构化文档标签。

```csharp
public IStructuredDocumentTag GetById(int id)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| id | Int32 | 结构化文档标签标识符。 |

### 评论

如果找不到具有指定标识符的结构化文档标签，则返回 null。

### 例子

展示如何获取结构化文档标签。

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// 通过Id获取结构化文档标签。
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// 根据标题获取结构化文档标签或范围标签。
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### 也可以看看

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* 部件 [Aspose.Words](../../../)


