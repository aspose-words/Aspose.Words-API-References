---
title: CertificateHolder Class
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.DigitalSignatures.CertificateHolder، وهي مفتاحك لإدارة مثيلات X509Certificate2 للتوقيعات الرقمية الآمنة.
type: docs
weight: 570
url: /ar/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

يمثل حامل**شهادة X5092** مثال.

لمعرفة المزيد، قم بزيارة[العمل مع التوقيعات الرقمية](https://docs.aspose.com/words/net/working-with-digital-signatures/) مقالة توثيقية.

```csharp
public class CertificateHolder
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | يعيد مثيلًا لـ**شهادة X5092** التي تحتوي على مفاتيح خاصة وعامة وسلسلة شهادات. |

## طُرق

| اسم | وصف |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(*byte[], SecureString*) | ينشئ`CertificateHolder` كائن يستخدم مجموعة بايتات من متجر PKCS12 وكلمة المرور الخاصة به. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(*byte[], string*) | ينشئ`CertificateHolder` كائن يستخدم مجموعة بايتات من متجر PKCS12 وكلمة المرور الخاصة به. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(*string, string*) | ينشئ`CertificateHolder`الكائن الذي يستخدم المسار إلى متجر PKCS12 وكلمة المرور الخاصة به. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(*string, string, string*) | ينشئ`CertificateHolder` الكائن باستخدام المسار إلى متجر PKCS12 وكلمة المرور الخاصة به والاسم المستعار باستخدام المفتاح الخاص والشهادة التي سيتم العثور عليها. |

## ملاحظات

`CertificateHolder` يمكن إنشاؤها بواسطة طرق المصنع الثابتة فقط. تحتوي على مثيل لـ**شهادة X5092** والتي تستخدم لإدخال المفاتيح الخاصة والعامة وسلاسل الشهادات إلى النظام. يتم تطبيق هذه الفئة في[`DigitalSignatureUtil`](../digitalsignatureutil/) و[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/) بدلاً من الأساليب القديمة مع X509Certificate2 كمعلمات.

## أمثلة

يوضح كيفية توقيع ملف مستند مشفر.

```csharp
// قم بإنشاء شهادة X.509 من متجر PKCS#12، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// قم بإنشاء تعليق وتاريخ وكلمة مرور فك التشفير والتي سيتم تطبيقها باستخدام توقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// تعيين اسم ملف النظام المحلي للمستند الإدخالي غير الموقع، واسم ملف الإخراج للنسخة الجديدة الموقعة رقميًا.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

يوضح كيفية التوقيع الرقمي على المستندات.

```csharp
// قم بإنشاء شهادة X.509 من متجر PKCS#12، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// قم بإنشاء تعليق وتاريخ سيتم تطبيقهما باستخدام توقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// أخذ مستند غير موقع من نظام الملفات المحلي عبر مجرى ملف،
// ثم قم بإنشاء نسخة موقعة منه يتم تحديدها من خلال اسم ملف مجرى ملف الإخراج.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

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

* مساحة الاسم [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../)
