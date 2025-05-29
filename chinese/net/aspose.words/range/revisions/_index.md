---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words for .NET
description: 探索范围修订。我们全面的修订集合，助您轻松追踪和管理物业变更，提升项目透明度。
type: docs
weight: 40
url: /zh/net/aspose.words/range/revisions/
---
## Range.Revisions property

获取此范围内存在的修订（跟踪的更改）的集合。

```csharp
public RevisionCollection Revisions { get; }
```

## 评论

返回的集合是一个“实时”集合，这意味着如果您删除包含 修订的文档部分，则已删除的修订将自动从该集合中消失。

## 例子

展示如何处理范围内的修订。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// 拒绝第一部分的修订。
doc.FirstSection.Range.Revisions.RejectAll();
```

### 也可以看看

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
