---
title: Range.Revisions
second_title: Aspose.Words for .NET API 参考
description: Range 财产. 获取此范围内存在的修订跟踪更改的集合
type: docs
weight: 40
url: /zh/net/aspose.words/range/revisions/
---
## Range.Revisions property

获取此范围内存在的修订（跟踪更改）的集合。

```csharp
public RevisionCollection Revisions { get; }
```

### 评论

返回的集合是“实时”集合，这意味着如果您删除文档中包含 修订版本的部分，则删除的修订版本将自动从此集合中消失。

### 例子

展示如何使用范围内的修订。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// 拒绝第一部分的修改。
doc.FirstSection.Range.Revisions.RejectAll();
```

### 也可以看看

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* 命名空间 [Aspose.Words](../../range/)
* 部件 [Aspose.Words](../../../)


