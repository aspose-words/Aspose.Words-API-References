---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words for .NET
description: 发现 ShapeBase HRef 属性，轻松管理形状的完整超链接地址，增强设计的交互性和功能性。
type: docs
weight: 250
url: /zh/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

获取或设置形状的完整超链接地址。

```csharp
public string HRef { get; set; }
```

## 评论

默认值为空字符串。

以下是此属性的有效值示例：

完整 URI：`https://www.aspose.com/`。

完整文件名：`C:\\我的文档\\SalesReport.doc`。

相对 URI：`../../../resource.txt`

相对文件名：`..\\我的文档\\销售报告.doc`。

在另一个文档中添加书签：`https://www.aspose.com/Products/Default.aspx#Suites`

本文档内的书签：`#BookmakName`。

## 例子

展示如何插入包含图像且为超链接的形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/”;
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + 左键单击 Microsoft Word 中的形状将打开一个新的 Web 浏览器窗口
// 并将我们带到“HRef”属性中的超链接。
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
