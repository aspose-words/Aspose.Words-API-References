---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: 用于 .NET 的 Aspose.Words
description: DigitalSignatureUtil LoadSignatures 方法. 从文档加载数字签名 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

从文档加载数字签名。

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 文档的路径。 |

### 返回值

数字签名的集合。如果文件未签名，则返回空集合。

## 例子

演示如何从数字签名文档加载签名。

```csharp
// 有两种方法可以使用 DigitalSignatureUtil 类加载签名文档的数字签名集合。
// 1 - 从本地文件系统文件名的文档加载：
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// 如果这个集合是非空的，那么我们可以验证该文档是数字签名的。
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - 从 FileStream 中的文档加载：
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

演示如何从数字签名文档中删除数字签名。

```csharp
// 使用 DigitalSignatureUtil 类去除数字签名有两种方式
// 通过将未签名的副本保存在本地文件系统的其他位置来从已签名的文档中提取。
// 1 - 通过文件名字符串确定签名文档和未签名副本的位置：
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - 通过文件流确定签名文档和未签名副本的位置：
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// 验证我们的两个输出文档都没有数字签名。
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### 也可以看看

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

使用流从文档中加载数字签名。

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 随文档流式传输。 |

### 返回值

数字签名的集合。如果文件未签名，则返回空集合。

## 例子

演示如何从数字签名文档加载签名。

```csharp
// 有两种方法可以使用 DigitalSignatureUtil 类加载签名文档的数字签名集合。
// 1 - 从本地文件系统文件名的文档加载：
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// 如果这个集合是非空的，那么我们可以验证该文档是数字签名的。
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - 从 FileStream 中的文档加载：
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

### 也可以看看

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
