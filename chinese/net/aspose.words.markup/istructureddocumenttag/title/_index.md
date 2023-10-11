---
title: IStructuredDocumentTag.Title
second_title: Aspose.Words for .NET API 参考
description: IStructuredDocumentTag 财产. 指定与此关联的友好名称 特殊测试 . 不能为空
type: docs
weight: 110
url: /zh/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

指定与此关联的友好名称 **特殊测试** . 不能为空。

```csharp
public string Title { get; set; }
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


