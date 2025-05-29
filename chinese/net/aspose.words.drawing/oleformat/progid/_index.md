---
title: OleFormat.ProgId
linktitle: ProgId
articleTitle: ProgId
second_title: Aspose.Words for .NET
description: 发现 OleFormat ProgId 属性以轻松管理和自定义 OLE 对象 ProgID，从而增强功能和无缝集成。
type: docs
weight: 90
url: /zh/net/aspose.words.drawing/oleformat/progid/
---
## OleFormat.ProgId property

获取或设置 OLE 对象的 ProgID。

```csharp
public string ProgId { get; set; }
```

## 评论

ProgID 属性并不总是存在于 Microsoft Word 文档中，因此不能依赖它。

不可能`无效的`。

默认值为空字符串。

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
