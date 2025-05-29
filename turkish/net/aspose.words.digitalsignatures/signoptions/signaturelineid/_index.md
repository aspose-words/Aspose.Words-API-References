---
title: SignOptions.SignatureLineId
linktitle: SignatureLineId
articleTitle: SignatureLineId
second_title: .NET için Aspose.Words
description: SignOptions'daki SignatureLineId özelliğini keşfedin. İmza satırlarını benzersiz bir GUID ile kolayca tanımlayın ve belge yönetimi verimliliğinizi artırın.
type: docs
weight: 50
url: /tr/net/aspose.words.digitalsignatures/signoptions/signaturelineid/
---
## SignOptions.SignatureLineId property

İmza satırı tanımlayıcısı. Varsayılan değer**Boş (tamamı sıfır) Kılavuz** .

```csharp
public Guid SignatureLineId { get; set; }
```

## Notlar

Ayarlandığında, ilişkilendirir[`SignatureLine`](../../../aspose.words.drawing/signatureline/) karşılık gelen[`DigitalSignature`](../../digitalsignature/) .

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

* class [SignOptions](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
