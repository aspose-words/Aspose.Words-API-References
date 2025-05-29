---
title: SignatureLineOptions.SignerTitle
linktitle: SignerTitle
articleTitle: SignerTitle
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SignerTitle في SignatureLineOptions لتخصيص عناوين المُوقّعين المقترحة بسهولة. حسّن احترافية مستندك بسهولة!
type: docs
weight: 80
url: /ar/net/aspose.words/signaturelineoptions/signertitle/
---
## SignatureLineOptions.SignerTitle property

يحصل على عنوان المُوقِّع المُقترح أو يُعيِّنه. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ).

```csharp
public string SignerTitle { get; set; }
```

## أمثلة

يوضح كيفية إضافة سطر توقيع إلى مستند، ثم التوقيع عليه باستخدام شهادة رقمية.

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
/// إنشاء نسخة من مستند المصدر الموقع باستخدام معلومات التوقيع المقدمة وشهادة X509.
/// </summary>
private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
    Signee signeeInfo, string certificatePath, string certificatePassword)
{
    Document document = new Document(srcDocumentPath);
    DocumentBuilder builder = new DocumentBuilder(document);

    // قم بتكوين وإدراج سطر التوقيع، وهو كائن في المستند سيعرض التوقيع الذي سنوقعه به.
    SignatureLineOptions signatureLineOptions = new SignatureLineOptions
    {
        Signer = signeeInfo.Name, 
        SignerTitle = signeeInfo.Position
    };

    SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
    signatureLine.Id = signeeInfo.PersonId;

    // أولاً، سوف نقوم بحفظ نسخة غير موقعة من مستندنا.
    builder.Document.Save(dstDocumentPath);

    CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

    SignOptions signOptions = new SignOptions
    {
        SignatureLineId = signeeInfo.PersonId,
        SignatureLineImage = signeeInfo.Image
    };

    //استبدل المستند غير الموقع الذي حفظناه أعلاه بإصدار موقع باستخدام الشهادة.
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

### أنظر أيضا

* class [SignatureLineOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
