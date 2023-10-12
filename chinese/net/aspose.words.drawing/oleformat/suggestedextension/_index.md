---
title: OleFormat.SuggestedExtension
second_title: Aspose.Words for .NET API 参考
description: OleFormat 财产. 如果要将当前嵌入对象保存到文件中则获取建议的文件扩展名
type: docs
weight: 120
url: /zh/net/aspose.words.drawing/oleformat/suggestedextension/
---
## OleFormat.SuggestedExtension property

如果要将当前嵌入对象保存到文件中，则获取建议的文件扩展名。

```csharp
public string SuggestedExtension { get; }
```

### 例子

演示如何将嵌入的 OLE 对象提取到文件中。

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// 第一个形状中的 OLE 对象是 Microsoft Excel 电子表格。
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// 我们的对象既不会自动更新，也不会被更新锁定。
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// 如果我们计划将 OLE 对象保存到本地文件系统中的文件中，
// 我们可以使用“SuggestedExtension”属性来确定要应用于该文件的文件扩展名。
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// 下面是将 OLE 对象保存到本地文件系统中的文件的两种方法。
// 1 - 通过流保存：
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - 直接将其保存到文件名：
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### 也可以看看

* class [OleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../oleformat/)
* 部件 [Aspose.Words](../../../)


