---
title: CertificateHolder Class
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.DigitalSignatures.CertificateHolder 班级. 代表持有者X509证书2实例 在 C#.
type: docs
weight: 370
url: /zh/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

代表持有者**X509证书2**实例.

要了解更多信息，请访问[使用数字签名](https://docs.aspose.com/words/net/working-with-digital-signatures/)文档文章。

```csharp
public class CertificateHolder
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | 返回以下实例**X509证书2**它保存私钥、公钥和证书链。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(*byte[], SecureString*) | 创建`CertificateHolder`使用 PKCS12 存储的字节数组及其密码的对象。 |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(*byte[], string*) | 创建`CertificateHolder`使用 PKCS12 存储的字节数组及其密码的对象。 |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(*string, string*) | 创建`CertificateHolder`使用 PKCS12 存储路径及其密码的对象。 |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(*string, string, string*) | 创建`CertificateHolder`使用 PKCS12 存储路径、其密码和别名的对象，通过使用该对象将找到私钥和证书。 |

## 评论

`CertificateHolder`只能通过静态工厂方法创建。 它包含一个实例**X509证书2**用于将私钥、公钥和证书链引入到系统中。 该类应用于[`DigitalSignatureUtil`](../digitalsignatureutil/)和[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/)用 代替过时的方法X509Certificate2作为参数。

## 例子

演示如何签署加密的文档文件。

```csharp
// 从 PKCS#12 存储创建 X.509 证书，该证书应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建评论、日期和解密密码，这些密码将与我们的新数字签名一起应用。
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// 为未签名的输入文档设置本地系统文件名，为其新的数字签名副本设置输出文件名。
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

展示如何对文档进行数字签名。

```csharp
// 从 PKCS#12 存储创建 X.509 证书，该证书应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建评论和日期，该评论和日期将与我们的新数字签名一起应用。
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// 通过文件流从本地文件系统获取未签名的文档，
// 然后创建由输出文件流的文件名确定的签名副本。
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

演示如何向文档添加签名行，然后使用数字证书对其进行签名。

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
        /// 创建使用提供的签名者信息和 X509 证书签名的源文档的副本。
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // 配置并插入签名行，这是文档中的一个对象，将显示我们用来签名的签名。
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

            // 用使用证书签名的版本覆盖我们上面保存的未签名文档。
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// 将图像转换为字节数组。
        /// </summary>
        private static byte[] ImageToByteArray(Image imageIn)
        {
            using (MemoryStream ms = new MemoryStream())
            {
                imageIn.Save(ms, ImageFormat.Png);
                return ms.ToArray();
            }
        }
#endif

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
            mSignees = new List<Signee>
            {
                #if NET48 || JAVA
                new Signee(Guid.NewGuid(), "Ron Williams", "Chief Executive Officer",
                    ImageToByteArray(Image.FromFile(ImageDir + "Logo.jpg"))),
                #elif NET5_0_OR_GREATER || __MOBILE__
                new Signee(Guid.NewGuid(), "Ron Williams", "Chief Executive Officer", 
                    SkiaSharp.SKBitmap.Decode(ImageDir + "Logo.jpg").Bytes),
                #endif

                #if NET48 || JAVA
                new Signee(Guid.NewGuid(), "Stephen Morse", "Head of Compliance",
                    ImageToByteArray(Image.FromFile(ImageDir + "Logo.jpg")))
                #elif NET5_0_OR_GREATER || __MOBILE__
                new Signee(Guid.NewGuid(), "Stephen Morse", "Head of Compliance", 
                    SkiaSharp.SKBitmap.Decode(ImageDir + "Logo.jpg").Bytes)
                #endif
            };
        }

        private static List<Signee> mSignees;
```

### 也可以看看

* 命名空间 [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../)
