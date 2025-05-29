---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words for .NET
description: 探索 Font NoProofing。避免对格式化文本进行拼写检查，打造更简洁的设计。精准专业地提升您的文档质量！
type: docs
weight: 280
url: /zh/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

当格式化字符不需要进行拼写检查时为真。

```csharp
public bool NoProofing { get; set; }
```

## 例子

展示如何防止 Microsoft Word 对文本进行拼写检查。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 通常，Microsoft Word 会使用锯齿状的红色下划线强调拼写错误。
// 我们可以取消设置“NoProofing”标志来创建一部分文本
// 绕过拼写检查器并完全禁用它。
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
