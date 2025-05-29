---
title: OleFormat.AutoUpdate
linktitle: AutoUpdate
articleTitle: AutoUpdate
second_title: Aspose.Words for .NET
description: 发现 Microsoft Word 中的 OleFormat AutoUpdate 属性，确保您的 OLE 对象链接保持最新并轻松提高文档的准确性。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/oleformat/autoupdate/
---
## OleFormat.AutoUpdate property

指定 Microsoft Word 中是否自动更新到 OLE 对象的链接。

```csharp
public bool AutoUpdate { get; set; }
```

## 评论

默认值为`错误的`。

## 例子

展示如何将嵌入的 OLE 对象提取到文件中。

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// 第一个形状中的 OLE 对象是 Microsoft Excel 电子表格。
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// 我们的对象既不是自动更新的，也不是锁定更新的。
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// 如果我们计划将 OLE 对象保存到本地文件系统中的文件中，
// 我们可以使用“SuggestedExtension”属性来确定要将哪个文件扩展名应用于文件。
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// 以下是将 OLE 对象保存到本地文件系统中的文件的两种方法。
// 1 - 通过流保存：
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - 直接保存为文件名：
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### 也可以看看

* class [OleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
