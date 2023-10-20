---
title: OleFormat.Save
linktitle: Save
articleTitle: Save
second_title: 用于 .NET 的 Aspose.Words
description: OleFormat Save 方法. 将嵌入对象的数据保存到指定的流中 在 C#.
type: docs
weight: 160
url: /zh/net/aspose.words.drawing/oleformat/save/
---
## Save(*Stream*) {#save}

将嵌入对象的数据保存到指定的流中。

```csharp
public void Save(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 保存对象数据的位置。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| InvalidOperationException | 如果您尝试保存链接对象，则抛出该异常。 |

## 评论

调用者有责任处理该流。

## 例子

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
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)

---

## Save(*string*) {#save_1}

将嵌入对象的数据保存到指定名称的文件中。

```csharp
public void Save(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 保存 OLE 对象数据的文件名。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| InvalidOperationException | 如果您尝试保存链接对象，则抛出该异常。 |

## 例子

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
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
