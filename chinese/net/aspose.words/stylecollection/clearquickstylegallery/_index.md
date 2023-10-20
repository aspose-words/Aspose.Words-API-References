---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: 用于 .NET 的 Aspose.Words
description: StyleCollection ClearQuickStyleGallery 方法. 从快速样式库面板中删除所有样式 在 C#.
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

演示如何从样式库面板中删除样式。

```csharp
Document doc = new Document();
// 请注意，删除样式目前仅适用于 DOCX 格式。
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### 也可以看看

* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
