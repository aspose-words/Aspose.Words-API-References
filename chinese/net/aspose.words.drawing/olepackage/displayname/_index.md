---
title: OlePackage.DisplayName
linktitle: DisplayName
articleTitle: DisplayName
second_title: Aspose.Words for .NET
description: 探索 OlePackage DisplayName 属性，轻松管理 OLE 包的显示名称。此关键功能可增强您的数据组织。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing/olepackage/displayname/
---
## OlePackage.DisplayName property

获取或设置 OLE 包显示名称。

```csharp
public string DisplayName { get; set; }
```

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

* class [OlePackage](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
