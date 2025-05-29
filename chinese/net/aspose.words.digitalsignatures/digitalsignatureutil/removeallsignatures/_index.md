---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: Aspose.Words for .NET
description: 使用 DigitalSignatureUtil 的 RemoveAllSignatures 方法轻松删除所有数字签名。轻松将您的签名文件转换为干净的未签名版本！
type: docs
weight: 20
url: /zh/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

从源文件中删除所有数字签名，并将未签名的文件写入目标文件。

以下格式与数字签名删除兼容： Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott。

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## 例子

展示如何从数字签名的文档中删除数字签名。

```csharp
// 使用 DigitalSignatureUtil 类删除数字签名有两种方法
// 通过将签名文档的未签名副本保存在本地文件系统的其他位置来获取签名文档。
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

// 验证我们的输出文档都没有数字签名。
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### 也可以看看

* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

从源流中的文档中删除所有数字签名，并将未签名的文档写入目标流。

**输出将被写入流的开头，并且流大小将根据内容长度进行更新。**

以下格式与数字签名删除兼容： Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott。

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## 例子

展示如何从数字签名的文档中删除数字签名。

```csharp
// 使用 DigitalSignatureUtil 类删除数字签名有两种方法
// 通过将签名文档的未签名副本保存在本地文件系统的其他位置来获取签名文档。
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

// 验证我们的输出文档都没有数字签名。
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### 也可以看看

* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
