---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: Aspose.Words for .NET
description: 发现揭示警告来源的WarningInfo Source属性，增强应用程序的可靠性和用户体验。
type: docs
weight: 20
url: /zh/net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

返回警告的来源。

```csharp
public WarningSource Source { get; }
```

## 例子

展示如何使用警告源。

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### 也可以看看

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
