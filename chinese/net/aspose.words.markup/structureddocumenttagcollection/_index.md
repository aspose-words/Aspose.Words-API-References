---
title: StructuredDocumentTagCollection Class
linktitle: StructuredDocumentTagCollection
articleTitle: StructuredDocumentTagCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.StructuredDocumentTagCollection 类，以有效管理结构化文档标签，增强您的文档处理能力。
type: docs
weight: 4760
url: /zh/net/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class

的集合[`IStructuredDocumentTag`](../istructureddocumenttag/)表示指定范围内的结构化文档标签的实例。

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class StructuredDocumentTagCollection : IEnumerable<IStructuredDocumentTag>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.markup/structureddocumenttagcollection/count/) { get; } | 返回集合中的结构化文档标签的数量。 |
| [Item](../../aspose.words.markup/structureddocumenttagcollection/item/) { get; } | 返回指定索引处的结构化文档标签。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetById](../../aspose.words.markup/structureddocumenttagcollection/getbyid/)(*int*) | 通过标识符返回结构化文档标签。 |
| [GetByTag](../../aspose.words.markup/structureddocumenttagcollection/getbytag/)(*string*) | 返回集合中遇到的第一个具有指定标签的结构化文档标签。 |
| [GetByTitle](../../aspose.words.markup/structureddocumenttagcollection/getbytitle/)(*string*) | 返回集合中遇到的第一个具有指定标题的结构化文档标签。 |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagcollection/getenumerator/)() | 返回一个枚举器对象。 |
| [Remove](../../aspose.words.markup/structureddocumenttagcollection/remove/)(*int*) | 删除具有指定标识符的结构化文档标签。 |
| [RemoveAt](../../aspose.words.markup/structureddocumenttagcollection/removeat/)(*int*) | 删除指定索引处的结构化文档标签。 |

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

* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
