---
title: ComHelper
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words for .NET
description: 探索 ComHelper，这个强大的构造函数可以轻松初始化新的类实例，从而提高您的编程效率和生产力。
type: docs
weight: 10
url: /zh/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

初始化此类的新实例。

```csharp
public ComHelper()
```

## 例子

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

* class [ComHelper](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
