---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.OlePackage 类以轻松管理 OLE 包属性并增强您的文档处理能力。
type: docs
weight: 1540
url: /zh/net/aspose.words.drawing/olepackage/
---
## OlePackage class

允许访问 OLE 包属性。

要了解更多信息，请访问[使用 Ole 对象](https://docs.aspose.com/words/net/working-with-ole-objects/)文档文章。

```csharp
public class OlePackage
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | 获取或设置 OLE 包显示名称。 |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | 获取或设置 OLE 包文件名。 |

## 评论

如果 OLE 处理程序未知，则 OLE 包是一种传统的、“未记录的”存储嵌入对象的方法。 早期的 Windows 版本（如 Windows 3.1、95 和 98）具有 Packager.exe 应用程序，可用于将任何类型的数据嵌入文档。 现在，此应用程序已被排除在 Windows 之外，但如果 OLE 处理程序丢失或未知，MS Word 和其他应用程序仍会使用它来嵌入数据。

## 例子

展示如何将 OLE 对象插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE 对象允许我们使用另一个已安装的应用程序打开本地文件系统中的其他文件
// 在我们的操作系统中，通过双击文档主体中包含 OLE 对象的形状。
// 在这种情况下，我们的外部文件将是一个 ZIP 存档。
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
