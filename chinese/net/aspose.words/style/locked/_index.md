---
title: Style.Locked
linktitle: Locked
articleTitle: Locked
second_title: Aspose.Words for .NET
description: 探索“样式锁定”属性，控制样式锁定，增强项目的设计灵活性和一致性。立即释放您的创造力！
type: docs
weight: 120
url: /zh/net/aspose.words/style/locked/
---
## Style.Locked property

指定此样式是否被锁定。

```csharp
public bool Locked { get; set; }
```

## 例子

展示如何锁定样式。

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];
if (!styleHeading1.Locked)
    styleHeading1.Locked = true;

doc.Save(ArtifactsDir + "Styles.LockStyle.docx");
```

### 也可以看看

* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
