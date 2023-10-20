---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: 用于 .NET 的 Aspose.Words
description: MailMerge RestartListsAtEachSection 财产. 获取或设置一个值该值指示是否在执行邮件合并后在每个部分重新启动列表 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

获取或设置一个值，该值指示是否在执行邮件合并后在每个部分重新启动列表。

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## 评论

默认值为**真的**.

## 例子

显示在执行邮件合并时如何控制是否在每个部分重新启动列表编号。

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
