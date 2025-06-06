---
title: ComHelper.Open
linktitle: Open
articleTitle: Open
second_title: Aspose.Words for .NET
description: 解锁与 ComHelper 的 Open 方法的无缝集成，使您的 COM 应用程序能够轻松地从文件中加载文档。
type: docs
weight: 20
url: /zh/net/aspose.words/comhelper/open/
---
## Open(*string*) {#open_1}

允许 COM 应用程序加载[`Document`](../../document/)来自文件。

```csharp
public Document Open(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 要加载的文档的文件名。 |

### 返回值

一个[`Document`](../../document/)代表 Word 文档的对象。

## 评论

此方法与调用[`Document`](../../document/)带有文件名参数的构造函数。

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

* class [Document](../../document/)
* class [ComHelper](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Open(*Stream*) {#open}

允许 COM 应用程序加载[`Document`](../../document/)来自流。

```csharp
public Document Open(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 包含要加载的文档的 .NET 流对象。 |

### 返回值

一个[`Document`](../../document/)代表 Word 文档的对象。

## 评论

此方法与调用[`Document`](../../document/)带有流参数的构造函数。

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

* class [Document](../../document/)
* class [ComHelper](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
