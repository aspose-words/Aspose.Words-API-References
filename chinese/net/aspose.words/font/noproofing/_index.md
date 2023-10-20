---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: 用于 .NET 的 Aspose.Words
description: Font NoProofing 财产. 当不对格式化字符进行拼写检查时为真 在 C#.
type: docs
weight: 280
url: /zh/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

当不对格式化字符进行拼写检查时为真。

```csharp
public bool NoProofing { get; set; }
```

## 例子

演示如何防止 Microsoft Word 对文本进行拼写检查。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 通常，Microsoft Word 使用锯齿状红色下划线强调拼写错误。
// 我们可以取消设置“NoProofing”标志来创建一部分文本
// 绕过拼写检查器，同时完全禁用它。
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
