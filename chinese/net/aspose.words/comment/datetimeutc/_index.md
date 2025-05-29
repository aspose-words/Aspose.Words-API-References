---
title: Comment.DateTimeUtc
linktitle: DateTimeUtc
articleTitle: DateTimeUtc
second_title: Aspose.Words for .NET
description: 发现评论 DateTimeUtc 属性，该属性可检索评论的准确 UTC 日期和时间，以便进行准确的跟踪和管理。
type: docs
weight: 50
url: /zh/net/aspose.words/comment/datetimeutc/
---
## Comment.DateTimeUtc property

获取发表评论的 UTC 日期和时间。

```csharp
public DateTime DateTimeUtc { get; }
```

## 评论

默认值为 MinValue

## 例子

展示如何获取 UTC 日期和时间。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

DateTime dateTime = DateTime.Now;
Comment comment = new Comment(doc, "John Doe", "J.D.", dateTime);
comment.SetText("My comment.");

builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.UtcDateTime.docx");
doc = new Document(ArtifactsDir + "Comment.UtcDateTime.docx");

comment = (Comment)doc.GetChild(NodeType.Comment, 0, true);
// DateTimeUtc 返回不带毫秒的数据。
Assert.AreEqual(dateTime.ToUniversalTime().ToString("yyyy-MM-dd hh:mm:ss"), comment.DateTimeUtc.ToString("yyyy-MM-dd hh:mm:ss"));
```

### 也可以看看

* class [Comment](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
