---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words for .NET
description: 探索 IStructuredDocumentTag Title 属性——为您的 SDT 定义一个用户友好的名称，提升文档清晰度。立即了解更多！
type: docs
weight: 140
url: /zh/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

指定与此相关的友好名称**特殊和差别待遇** . 不能为空。

```csharp
public string Title { get; set; }
```

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

* interface [IStructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
