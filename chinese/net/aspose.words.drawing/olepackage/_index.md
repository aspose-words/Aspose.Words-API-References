---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.OlePackage 班级. 允许访问 OLE 包属性 在 C#.
type: docs
weight: 1160
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

OLE 包是一种传统且“未记录”的方式，用于在 OLE 处理程序未知的情况下存储嵌入对象。 早期 Windows 版本（例如 Windows 3.1、95 和 98）具有 Packager.exe 应用程序，可用于将任何类型的数据嵌入到文档中. 现在此应用程序已从 Windows 中排除，但如果 OLE 处理程序丢失或未知，MS Word 和其他应用程序仍使用它来嵌入数据。

## 例子

显示如何将 OLE 对象插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE 对象允许我们使用另一个已安装的应用程序打开本地文件系统中的其他文件
// 在我们的操作系统中，双击文档正文中包含 OLE 对象的形状。
// 在这种情况下，我们的外部文件将是 ZIP 存档。
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
