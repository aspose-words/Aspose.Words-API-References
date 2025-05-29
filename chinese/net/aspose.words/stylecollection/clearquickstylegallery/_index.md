---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: Aspose.Words for .NET
description: 使用 StyleCollection 的 ClearQuickStyleGallery 方法，轻松清除快速样式库中的样式。立即简化您的设计流程！
type: docs
weight: 80
url: /zh/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

从快速样式库面板中删除所有样式。

```csharp
public void ClearQuickStyleGallery()
```

## 例子

展示如何从样式库面板中删除样式。

```csharp
Document doc = new Document();
// 请注意，目前删除样式仅适用于 DOCX 格式。
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### 也可以看看

* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
