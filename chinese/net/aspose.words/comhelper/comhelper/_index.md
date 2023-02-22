---
title: ComHelper.ComHelper
second_title: Aspose.Words for .NET API 参考
description: ComHelper 构造函数. 初始化这个类的一个新实例
type: docs
weight: 10
url: /zh/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

初始化这个类的一个新实例。

```csharp
public ComHelper()
```

### 例子

演示如何使用 ComHelper 类打开文档。

```csharp
// ComHelper 类允许我们从 COM 客户端加载文档。
ComHelper comHelper = new ComHelper();

// 1 - 使用本地系统文件名：
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - 从流中：
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### 也可以看看

* class [ComHelper](../)
* 命名空间 [Aspose.Words](../../comhelper/)
* 部件 [Aspose.Words](../../../)


