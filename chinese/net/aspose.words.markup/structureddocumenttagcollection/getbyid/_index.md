---
title: StructuredDocumentTagCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: Aspose.Words for .NET
description: 使用 GetById 方法轻松检索结构化文档标签。快速访问您的数据，提升文档管理效率。
type: docs
weight: 30
url: /zh/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

通过标识符返回结构化文档标签。

```csharp
public IStructuredDocumentTag GetById(int id)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| id | Int32 | 结构化文档标签标识符。 |

## 评论

如果找不到具有指定标识符的结构化文档标签，则返回 null。

## 例子

展示如何获取结构化文档标签。

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// 通过Id获取结构化文档标签。
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// 通过标题获取结构化文档标签或范围标签。
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### 也可以看看

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
