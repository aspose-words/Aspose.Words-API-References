---
title: CertificateHolder Class
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.DigitalSignatures.CertificateHolder 类，这是管理安全数字签名的 X509Certificate2 实例的关键。
type: docs
weight: 570
url: /zh/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

代表持有**X509证书2**实例.

要了解更多信息，请访问[使用数字签名](https://docs.aspose.com/words/net/working-with-digital-signatures/)文档文章。

```csharp
public class CertificateHolder
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | 返回**X509证书2**其中包含私钥、公钥和证书链。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(*byte[], SecureString*) | 创建`CertificateHolder`使用 PKCS12 存储的字节数组及其密码的对象。 |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(*byte[], string*) | 创建`CertificateHolder`使用 PKCS12 存储的字节数组及其密码的对象。 |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(*string, string*) | 创建`CertificateHolder`对象使用 PKCS12 存储路径及其密码。 |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(*string, string, string*) | 创建`CertificateHolder`对象使用 PKCS12 存储的路径、其密码以及将通过其找到私钥和证书的别名。 |

## 评论

`CertificateHolder`只能通过静态工厂方法创建。 它包含一个实例**X509证书2**用于将私钥、公钥和证书链引入系统。 此类应用于[`DigitalSignatureUtil`](../digitalsignatureutil/)和[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/)用 代替过时的方法X509Certificate2作为参数。

## 例子

显示如何签署加密文档文件。

```csharp
// 从 PKCS#12 存储区创建 X.509 证书，该证书应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建将与我们的新数字签名一起应用的评论、日期和解密密码。
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// 为未签名的输入文档设置本地系统文件名，并为其新的数字签名副本设置输出文件名。
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

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

* 命名空间 [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../)
