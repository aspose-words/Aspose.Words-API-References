---
title: DigitalSignatureUtil.Sign
linktitle: Sign
articleTitle: Sign
second_title: Aspose.Words لـ .NET
description: وقّع مستنداتك بسهولة باستخدام طريقة التوقيع من DigitalSignatureUtil. طبّق التوقيعات الرقمية بأمان باستخدام CertificateHolder وSignOptions.
type: docs
weight: 30
url: /ar/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_1}

يوقع مستند المصدر باستخدام المحدد[`CertificateHolder`](../../certificateholder/) و[`SignOptions`](../../signoptions/) مع التوقيع الرقمي ويكتب المستند الموقع إلى مجرى الوجهة.

التنسيقات المدعومة هي: Doc ، Dot ، Docx ، Dotx ، Docm ، Dotm ، Odt ، Ott.

**سيتم كتابة الإخراج في بداية التدفق وسيتم تحديث حجم التدفق بطول المحتوى.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcStream | Stream | التدفق الذي يحتوي على المستند الذي يجب التوقيع عليه. |
| dstStream | Stream | المسار الذي سيتم كتابة المستند الموقّع إليه. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) الكائن الذي يحتوي على شهادة تم استخدامها لتوقيع الملف. يجب أن تحتوي الشهادة الموجودة في الحامل على مفاتيح خاصة ويجب أن تحتوي على علامة X509KeyStorageFlags.Exportable. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) كائن مع خيارات توقيع مختلفة. |

## أمثلة

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

### أنظر أيضا

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_3}

يوقع مستند المصدر باستخدام المحدد[`CertificateHolder`](../../certificateholder/) و[`SignOptions`](../../signoptions/) مع التوقيع الرقمي ويكتب المستند الموقع إلى ملف الوجهة.

التنسيقات المدعومة هي: Doc ، Dot ، Docx ، Dotx ، Docm ، Dotm ، Odt ، Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcFileName | String | اسم ملف المستند الذي سيتم التوقيع عليه. |
| dstFileName | String | اسم ملف إخراج المستند الموقع. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) الكائن الذي يحتوي على شهادة تم استخدامها لتوقيع الملف. يجب أن تحتوي الشهادة الموجودة في الحامل على مفاتيح خاصة ويجب أن تحتوي على علامة X509KeyStorageFlags.Exportable. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) كائن مع خيارات توقيع مختلفة. |

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

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)

---

## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/)*) {#sign}

يوقع مستند المصدر باستخدام المحدد[`CertificateHolder`](../../certificateholder/) مع التوقيع الرقمي ويكتب المستند الموقّع إلى مجرى الوجهة.

التنسيقات المدعومة هي: Doc ، Dot ، Docx ، Dotx ، Docm ، Dotm ، Odt ، Ott.

**سيتم كتابة الإخراج في بداية التدفق وسيتم تحديث حجم التدفق بطول المحتوى.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcStream | Stream | التدفق الذي يحتوي على المستند الذي يجب التوقيع عليه. |
| dstStream | Stream | المسار الذي سيتم كتابة المستند الموقّع إليه. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) الكائن الذي يحتوي على شهادة تم استخدامها لتوقيع الملف. يجب أن تحتوي الشهادة الموجودة في الحامل على مفاتيح خاصة ويجب أن تحتوي على علامة X509KeyStorageFlags.Exportable. |

## أمثلة

يوضح كيفية توقيع المستندات باستخدام شهادات X.509.

```csharp
//التأكد من عدم توقيع المستند.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// قم بإنشاء كائن CertificateHolder من ملف PKCS12، والذي سنستخدمه لتوقيع المستند.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// هناك طريقتان لحفظ نسخة موقعة من مستند في نظام الملفات المحلي:
// 1 - تعيين مستند من خلال اسم ملف النظام المحلي وحفظ نسخة موقعة في موقع محدد بواسطة اسم ملف آخر.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - أخذ مستند من مجرى وحفظ نسخة موقعة في مجرى آخر.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// يرجى التأكد من صحة كافة التوقيعات الرقمية للوثيقة والتحقق من تفاصيلها.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### أنظر أيضا

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/)*) {#sign_2}

يوقع مستند المصدر باستخدام المحدد[`CertificateHolder`](../../certificateholder/) مع التوقيع الرقمي ويكتب المستند الموقع إلى ملف الوجهة.

التنسيقات المدعومة هي: Doc ، Dot ، Docx ، Dotx ، Docm ، Dotm ، Odt ، Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcFileName | String | اسم ملف المستند الذي سيتم التوقيع عليه. |
| dstFileName | String | اسم ملف إخراج المستند الموقع. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) الكائن الذي يحتوي على شهادة تم استخدامها لتوقيع الملف. يجب أن تحتوي الشهادة الموجودة في الحامل على مفاتيح خاصة ويجب أن تحتوي على علامة X509KeyStorageFlags.Exportable. |

## أمثلة

يوضح كيفية توقيع المستندات باستخدام شهادات X.509.

```csharp
//التأكد من عدم توقيع المستند.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// قم بإنشاء كائن CertificateHolder من ملف PKCS12، والذي سنستخدمه لتوقيع المستند.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// هناك طريقتان لحفظ نسخة موقعة من مستند في نظام الملفات المحلي:
// 1 - تعيين مستند من خلال اسم ملف النظام المحلي وحفظ نسخة موقعة في موقع محدد بواسطة اسم ملف آخر.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - أخذ مستند من مجرى وحفظ نسخة موقعة في مجرى آخر.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// يرجى التأكد من صحة كافة التوقيعات الرقمية للوثيقة والتحقق من تفاصيلها.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### أنظر أيضا

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
