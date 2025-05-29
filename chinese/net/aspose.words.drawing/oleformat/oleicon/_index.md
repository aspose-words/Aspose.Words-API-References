---
title: OleFormat.OleIcon
linktitle: OleIcon
articleTitle: OleIcon
second_title: Aspose.Words for .NET
description: 发现 OleFormat OleIcon 属性，控制 OLE 对象显示为图标或内容，以增强用户体验并在应用程序中无缝集成。
type: docs
weight: 70
url: /zh/net/aspose.words.drawing/oleformat/oleicon/
---
## OleFormat.OleIcon property

获取 OLE 对象的绘制方式。当`真的`时，OLE 对象显示为图标。 当`错误的`，OLE 对象显示为内容。

```csharp
public bool OleIcon { get; }
```

## 评论

Aspose.Words 不允许设置此属性，以避免混淆。如果您能够在 Aspose.Words 中更改 的绘制方式，Microsoft Word 仍会以其原始 的绘制方式显示 OLE 对象，直到您在 Microsoft Word 中编辑或更新该 OLE 对象为止。

## 例子

展示如何插入链接和非链接的 OLE 对象。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将 Microsoft Visio 绘图作为 OLE 对象嵌入到文档中。
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// 插入本地文件系统中的文件链接并将其显示为图标。
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// 插入 OLE 对象会创建存储这些对象的形状。
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// 如果形状包含 OLE 对象，它将具有有效的“OleFormat”属性，
// 我们可以使用它来验证形状的某些方面。
OleFormat oleFormat = shapes[0].OleFormat;

Assert.AreEqual(false, oleFormat.IsLink);
Assert.AreEqual(false, oleFormat.OleIcon);

oleFormat = shapes[1].OleFormat;

Assert.AreEqual(true, oleFormat.IsLink);
Assert.AreEqual(true, oleFormat.OleIcon);

Assert.True(oleFormat.SourceFullName.EndsWith(@"Images" + Path.DirectorySeparatorChar + "Microsoft Visio drawing.vsd"));
Assert.AreEqual("", oleFormat.SourceItem);

Assert.AreEqual("Microsoft Visio drawing.vsd", oleFormat.IconCaption);

doc.Save(ArtifactsDir + "Shape.OleLinks.docx");

// 如果对象包含 OLE 数据，我们可以使用流访问它。
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### 也可以看看

* class [OleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
