---
title: DigitalSignatureUtil.LoadSignatures
second_title: Aspose.Words for .NET API 参考
description: DigitalSignatureUtil 方法. 从文档加载数字签名
type: docs
weight: 10
url: /zh/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(string) {#loadsignatures_1}

从文档加载数字签名。

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 文档的路径。 |

### 返回值

数字签名的集合。如果文件未签名，则返回空集合。

### 例子

演示如何从数字签名文档加载签名。

```csharp
// 使用 DigitalSignatureUtil 类加载签名文档的数字签名集合有两种方法。
// 1 - 从本地文件系统文件名的文档加载：
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// 如果这个集合非空，那么我们可以验证文档是否经过数字签名。
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - 从 FileStream 中加载文档：
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

演示如何从数字签名文档中删除数字签名。

```csharp
// 使用DigitalSignatureUtil类去除数字签名有两种方法
// 通过将已签名文档的未签名副本保存在本地文件系统中的其他位置来获取该文档。
// 1 - 通过文件名字符串确定已签名文档和未签名副本的位置：
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - 通过文件流确定已签名文档和未签名副本的位置：
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// 验证我们的输出文档没有数字签名。
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### 也可以看看

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* 部件 [Aspose.Words](../../../)

---

## LoadSignatures(Stream) {#loadsignatures}

使用流从文档加载数字签名。

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 随文档一起流式传输。 |

### 返回值

数字签名的集合。如果文件未签名，则返回空集合。

### 例子

演示如何从数字签名文档加载签名。

```csharp
// 使用 DigitalSignatureUtil 类加载签名文档的数字签名集合有两种方法。
// 1 - 从本地文件系统文件名的文档加载：
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// 如果这个集合非空，那么我们可以验证文档是否经过数字签名。
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - 从 FileStream 中加载文档：
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

### 也可以看看

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* 部件 [Aspose.Words](../../../)


