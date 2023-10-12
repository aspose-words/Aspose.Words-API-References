---
title: DigitalSignatureUtil.RemoveAllSignatures
second_title: Aspose.Words for .NET API 参考
description: DigitalSignatureUtil 方法. 从源文件中删除所有数字签名并将未签名的文件写入目标文件
type: docs
weight: 20
url: /zh/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(string, string) {#removeallsignatures_1}

从源文件中删除所有数字签名并将未签名的文件写入目标文件。

以下格式兼容数字签名删除： Doc, Dot, Docx, Dotx, Docm, Odt, Ott。

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

### 例子

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

* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* 部件 [Aspose.Words](../../../)

---

## RemoveAllSignatures(Stream, Stream) {#removeallsignatures}

从源流中的文档中删除所有数字签名，并将未签名的文档写入目标流。

**输出将被写入流的开头，并且流大小将根据内容长度进行更新。**

以下格式兼容数字签名删除： Doc, Dot, Docx, Dotx, Docm, Odt, Ott。

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

### 例子

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

* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* 部件 [Aspose.Words](../../../)


