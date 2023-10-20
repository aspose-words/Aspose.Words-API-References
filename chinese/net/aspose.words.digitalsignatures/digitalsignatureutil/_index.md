---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.DigitalSignatures.DigitalSignatureUtil 班级. 提供签署文档的方法 在 C#.
type: docs
weight: 410
url: /zh/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

提供签署文档的方法。

要了解更多信息，请访问[使用数字签名](https://docs.aspose.com/words/net/working-with-digital-signatures/)文档文章。

```csharp
public static class DigitalSignatureUtil
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | 使用流从文档加载数字签名。 |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | 从文档加载数字签名。 |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | 从源流中的文档中删除所有数字签名，并将未签名的文档写入目标流。 |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | 从源文件中删除所有数字签名并将未签名的文件写入目标文件。 |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | 使用给定的源文档签名[`CertificateHolder`](../certificateholder/)带有数字签名 并将签名文档写入目标流. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | 使用给定的源文档签名[`CertificateHolder`](../certificateholder/)带有数字签名 并将签名文档写入目标文件. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | 使用给定的源文档签名[`CertificateHolder`](../certificateholder/)和[`SignOptions`](../signoptions/) 带有数字签名并将签名文档写入目标流。 |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | 使用给定的源文档签名[`CertificateHolder`](../certificateholder/)和[`SignOptions`](../signoptions/) 带有数字签名并将签名文档写入目标文件。 |

## 评论

由于数字签名适用于文件内容而不是文档对象模型，因此这些方法被放入单独的类中。

支持的格式有Doc和Docx。

## 例子

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

* 命名空间 [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../)
