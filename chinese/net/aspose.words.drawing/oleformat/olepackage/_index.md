---
title: OleFormat.OlePackage
second_title: Aspose.Words for .NET API 参考
description: OleFormat 财产. 提供对OlePackage如果 OLE 对象是 OLE 包 返回无效的否则.
type: docs
weight: 80
url: /zh/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

提供对[`OlePackage`](../../olepackage/)如果 OLE 对象是 OLE 包。 返回`无效的`否则.

```csharp
public OlePackage OlePackage { get; }
```

### 评论

OLE 包是一项传统技术，允许将 Windows 系统的 OLE 注册表中不存在的任何文件格式包装到通用包中，从而允许将几乎所有内容嵌入到文档中。 请参阅[`OlePackage`](../../olepackage/)输入以获取更多信息。

### 例子

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

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../oleformat/)
* 部件 [Aspose.Words](../../../)


