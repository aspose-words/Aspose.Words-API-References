---
title: OleFormat.SourceItem
linktitle: SourceItem
articleTitle: SourceItem
second_title: 用于 .NET 的 Aspose.Words
description: OleFormat SourceItem 财产. 获取或设置用于标识正在链接的源文件部分的字符串 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.drawing/oleformat/sourceitem/
---
## OleFormat.SourceItem property

获取或设置用于标识正在链接的源文件部分的字符串。

```csharp
public string SourceItem { get; set; }
```

## 评论

默认值为空字符串。

例如，如果源文件是 Microsoft Excel 工作簿，则`SourceItem`如果 OLE 对象仅包含 工作表中的几个单元格， 属性可能会返回“Workbook1!R3C1:R4C2”。

## 例子

显示如何插入链接和未链接的 OLE 对象。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将 Microsoft Visio 绘图作为 OLE 对象嵌入到文档中。
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// 在本地文件系统中插入文件的链接，并显示为图标。
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// 插入 OLE 对象会创建存储这些对象的形状。
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// 如果一个形状包含一个 OLE 对象，它将有一个有效的“OleFormat”属性，
// 我们可以用它来验证形状的某些方面。
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
