---
title: MailMerge.RestartListsAtEachSection
second_title: Aspose.Words for .NET API 参考
description: MailMerge 财产. 获取或设置一个值该值指示执行邮件合并后是否在每个部分重新启动列表
type: docs
weight: 110
url: /zh/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

获取或设置一个值，该值指示执行邮件合并后是否在每个部分重新启动列表。

```csharp
public bool RestartListsAtEachSection { get; set; }
```

### 评论

默认值为`真的`.

### 例子

显示如何控制执行邮件合并时是否在每个部分重新开始列表编号。

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)


