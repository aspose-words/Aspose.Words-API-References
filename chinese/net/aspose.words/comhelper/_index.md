---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.ComHelper 实现无缝文档集成。利用强大的功能，轻松加载和管理 COM 客户端文档。
type: docs
weight: 410
url: /zh/net/aspose.words/comhelper/
---
## ComHelper class

为 COM 客户端提供将文档加载到 Aspose.Words 中的方法。

```csharp
public class ComHelper
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ComHelper](comhelper/)() | 初始化此类的新实例。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | 允许 COM 应用程序加载[`Document`](../document/)来自流。 |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | 允许 COM 应用程序加载[`Document`](../document/)来自文件。 |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | 允许 COM 应用程序加载[`Document`](../document/)来自 IStream 对象。 |

## 评论

使用`ComHelper`将文档从文件或流加载到 中的类[`Document`](../document/)COM 应用程序中的对象。

这[`Document`](../document/)类提供了一个默认构造函数来创建新的文档 ，还提供了重载构造函数来从文件或流加载文档。 如果您在 .NET 应用程序中使用 Aspose.Words，则可以使用所有[`Document`](../document/) 构造函数，但如果您正在 COM 应用程序中使用 Aspose.Words， 仅默认[`Document`](../document/)构造函数可用。

## 例子

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

展示如何使用 ComHelper 类打开文档。

```csharp
// ComHelper 类允许我们从 COM 客户端内部加载文档。
ComHelper comHelper = new ComHelper();

// 1 - 使用本地系统文件名：
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - 来自流：
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
