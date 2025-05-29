---
title: DigitalSignatureUtil.Sign
linktitle: Sign
articleTitle: Sign
second_title: Aspose.Words for .NET
description: 使用 DigitalSignatureUtil 的 Sign 方法轻松签署您的文档。使用 CertificateHolder 和 SignOptions 安全地应用数字签名。
type: docs
weight: 30
url: /zh/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_1}

使用给定的签名源文档[`CertificateHolder`](../../certificateholder/)和[`SignOptions`](../../signoptions/) 带有数字签名并将签名文档写入目标流。

支持的格式为： Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott。

**输出将被写入流的开头，并且流大小将根据内容长度进行更新。**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcStream | Stream | 包含要签名的文件的流。 |
| dstStream | Stream | 签名文档将被写入的流。 |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/)用于签署文件的带有证书的对象。 持有者的证书必须包含私钥并设置了 X509KeyStorageFlags.Exportable 标志。 |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/)具有各种签名选项的对象。 |

## 例子

展示如何对文档进行数字签名。

```csharp
// 从 PKCS#12 存储区创建 X.509 证书，该证书应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建将与我们的新数字签名一起应用的评论和日期。
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// 通过文件流从本地文件系统获取未签名的文档，
// 然后根据输出文件流的文件名创建它的签名副本。
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### 也可以看看

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_3}

使用给定的签名源文档[`CertificateHolder`](../../certificateholder/)和[`SignOptions`](../../signoptions/) 带有数字签名并将签名文档写入目标文件。

支持的格式为： Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott。

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcFileName | String | 待签名文件的文件名。 |
| dstFileName | String | 签名文档输出的文件名。 |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/)用于签署文件的带有证书的对象。 持有者的证书必须包含私钥并设置了 X509KeyStorageFlags.Exportable 标志。 |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/)具有各种签名选项的对象。 |

## 例子

展示如何在文档中添加签名行，然后使用数字证书对其进行签名。

```csharp
[Description("WORDSNET-16868")]
public static void Sign()
{
    string signeeName = "Ron Williams";
    string srcDocumentPath = MyDir + "Document.docx";
    string dstDocumentPath = ArtifactsDir + "SignDocumentCustom.Sign.docx";
    string certificatePath = MyDir + "morzal.pfx";
    string certificatePassword = "aw";

    CreateSignees();

    Signee signeeInfo = mSignees.Find(c => c.Name == signeeName);

    if (signeeInfo != null)
        SignDocument(srcDocumentPath, dstDocumentPath, signeeInfo, certificatePath, certificatePassword);
    else
        Assert.Fail("Signee does not exist.");
}

/// <summary>
/// 使用提供的签名者信息和 X509 证书创建签名的源文档的副本。
/// </summary>
private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
    Signee signeeInfo, string certificatePath, string certificatePassword)
{
    Document document = new Document(srcDocumentPath);
    DocumentBuilder builder = new DocumentBuilder(document);

    // 配置并插入签名行，即文档中的一个对象，它将显示我们用来签名的签名。
    SignatureLineOptions signatureLineOptions = new SignatureLineOptions
    {
        Signer = signeeInfo.Name, 
        SignerTitle = signeeInfo.Position
    };

    SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
    signatureLine.Id = signeeInfo.PersonId;

    // 首先，我们将保存文档的未签名版本。
    builder.Document.Save(dstDocumentPath);

    CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

    SignOptions signOptions = new SignOptions
    {
        SignatureLineId = signeeInfo.PersonId,
        SignatureLineImage = signeeInfo.Image
    };

    // 用证书签名的版本覆盖我们上面保存的未签名文档。
    DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
}

public class Signee
{
    public Guid PersonId { get; set; }
    public string Name { get; set; }
    public string Position { get; set; }
    public byte[] Image { get; set; }

    public Signee(Guid guid, string name, string position, byte[] image)
    {
        PersonId = guid;
        Name = name;
        Position = position;
        Image = image;
    }
}

private static void CreateSignees()
{
    var signImagePath = ImageDir + "Logo.jpg";

    mSignees = new List<Signee>
    {
        new Signee(Guid.NewGuid(), "Ron Williams", "Chief Executive Officer", TestUtil.ImageToByteArray(signImagePath)),
        new Signee(Guid.NewGuid(), "Stephen Morse", "Head of Compliance", TestUtil.ImageToByteArray(signImagePath))
    };
}

private static List<Signee> mSignees;
```

### 也可以看看

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)

---

## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/)*) {#sign}

使用给定的签名源文档[`CertificateHolder`](../../certificateholder/)使用数字签名 并将签名文档写入目标流。

支持的格式为： Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott。

**输出将被写入流的开头，并且流大小将根据内容长度进行更新。**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcStream | Stream | 包含要签名的文件的流。 |
| dstStream | Stream | 签名文档将被写入的流。 |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/)用于签署文件的带有证书的对象。 持有者的证书必须包含私钥并设置了 X509KeyStorageFlags.Exportable 标志。 |

## 例子

展示如何使用 X.509 证书签署文档。

```csharp
// 验证文档未签名。
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// 从 PKCS12 文件创建一个 CertificateHolder 对象，我们将使用它来签署文档。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// 有两种方法可以将文档的签名副本保存到本地文件系统：
// 1 - 通过本地系统文件名指定文档，并将签名副本保存在另一个文件名指定的位置。
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - 从流中获取文档并将签名的副本保存到另一个流。
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 请验证所有文档的数字签名是否有效并检查其详细信息。
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### 也可以看看

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/)*) {#sign_2}

使用给定的签名源文档[`CertificateHolder`](../../certificateholder/)使用数字签名 并将签名文档写入目标文件。

支持的格式为： Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott。

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcFileName | String | 待签名文件的文件名。 |
| dstFileName | String | 签名文档输出的文件名。 |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/)用于签署文件的带有证书的对象。 持有者的证书必须包含私钥并设置了 X509KeyStorageFlags.Exportable 标志。 |

## 例子

展示如何使用 X.509 证书签署文档。

```csharp
// 验证文档未签名。
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// 从 PKCS12 文件创建一个 CertificateHolder 对象，我们将使用它来签署文档。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// 有两种方法可以将文档的签名副本保存到本地文件系统：
// 1 - 通过本地系统文件名指定文档，并将签名副本保存在另一个文件名指定的位置。
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - 从流中获取文档并将签名的副本保存到另一个流。
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 请验证所有文档的数字签名是否有效并检查其详细信息。
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### 也可以看看

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
