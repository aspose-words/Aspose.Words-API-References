---
title: StructuredDocumentTagCollection.GetByTitle
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTagCollection 方法. 返回在具有指定标题的集合中遇到的第一个结构化文档标签
type: docs
weight: 50
url: /zh/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

返回在具有指定标题的集合中遇到的第一个结构化文档标签。

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| title | String | 结构化文档标签的标题。 |

### 评论

如果找不到具有指定标题的结构化文档标签，则返回 null。

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


