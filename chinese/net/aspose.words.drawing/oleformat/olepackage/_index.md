---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words for .NET
description: 轻松访问 OLE 对象的 OlePackage 属性。与 OLE 包无缝集成，增强数据处理能力。
type: docs
weight: 80
url: /zh/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

提供访问权限[`OlePackage`](../../olepackage/)如果 OLE 对象是 OLE 包。 返回`无效的`否则。

```csharp
public OlePackage OlePackage { get; }
```

## 评论

OLE 包是一种传统技术，允许将 Windows 系统的 OLE 注册表中不存在的任何文件格式包装到通用包中，从而可以将几乎任何内容嵌入到文档中。 参见[`OlePackage`](../../olepackage/)输入更多信息。

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

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
