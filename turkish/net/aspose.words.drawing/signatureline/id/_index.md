---
title: SignatureLine.Id
linktitle: Id
articleTitle: Id
second_title: .NET için Aspose.Words
description: Sorunsuz belge entegrasyonu ve gelişmiş kullanıcı deneyimi için imza satırı tanımlayıcılarını kolayca yönetmek ve özelleştirmek amacıyla SignatureLine Id özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/signatureline/id/
---
## SignatureLine.Id property

Bu imza satırı için tanımlayıcıyı alır veya ayarlar.

Bu tanımlayıcı, belgeyi kullanarak imzalarken dijital imzayla ilişkilendirilebilir.[`DigitalSignatureUtil`](../../../aspose.words.digitalsignatures/digitalsignatureutil/). Bu değer benzersiz olmalı ve varsayılan olarak rastgele yeni Guid (NewGuid).

```csharp
public Guid Id { get; set; }
```

## Örnekler

Bir belgeye imza satırının nasıl ekleneceğini ve ardından dijital sertifika kullanılarak nasıl imzalanacağını gösterir.

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
/// Sağlanan imzalayan bilgileri ve X509 sertifikası kullanılarak imzalanmış bir kaynak belgenin kopyasını oluşturur.
/// </summary>
private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
    Signee signeeInfo, string certificatePath, string certificatePassword)
{
    Document document = new Document(srcDocumentPath);
    DocumentBuilder builder = new DocumentBuilder(document);

    // Belgeye imzamızı koyacağımız bir nesne olan imza satırını yapılandırın ve ekleyin.
    SignatureLineOptions signatureLineOptions = new SignatureLineOptions
    {
        Signer = signeeInfo.Name, 
        SignerTitle = signeeInfo.Position
    };

    SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
    signatureLine.Id = signeeInfo.PersonId;

    // İlk olarak belgemizin imzasız halini kaydedeceğiz.
    builder.Document.Save(dstDocumentPath);

    CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

    SignOptions signOptions = new SignOptions
    {
        SignatureLineId = signeeInfo.PersonId,
        SignatureLineImage = signeeInfo.Image
    };

    // Yukarıda kaydettiğimiz imzasız belgenin üzerine sertifika kullanılarak imzalanmış bir sürüm yaz.
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

### Ayrıca bakınız

* class [SignatureLine](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
