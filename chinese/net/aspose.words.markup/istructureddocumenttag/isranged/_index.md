---
title: IStructuredDocumentTag.IsRanged
second_title: Aspose.Words for .NET API 参考
description: IStructuredDocumentTag 方法. 如果此实例是范围结构化文档标记则返回 true
type: docs
weight: 140
url: /zh/net/aspose.words.markup/istructureddocumenttag/isranged/
---
## IStructuredDocumentTag.IsRanged method

如果此实例是范围结构化文档标记，则返回 true。

```csharp
public bool IsRanged()
```

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

* interface [IStructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../istructureddocumenttag/)
* 部件 [Aspose.Words](../../../)


