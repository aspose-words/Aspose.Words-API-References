---
title: Document.DigitalSignatures
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. الحصول على مجموعة التوقيعات الرقمية لهذا المستند ونتائج التحقق من صحتها.
type: docs
weight: 100
url: /ar/net/aspose.words/document/digitalsignatures/
---
## Document.DigitalSignatures property

الحصول على مجموعة التوقيعات الرقمية لهذا المستند ونتائج التحقق من صحتها.

```csharp
public DigitalSignatureCollection DigitalSignatures { get; }
```

### ملاحظات

تحتوي هذه المجموعة على تواقيع رقمية تم تحميلها من المستند الأصلي . لن يتم حفظ هذه التوقيعات الرقمية عند حفظ هذا[`Document`](../) object في ملف أو دفق لأن الحفظ أو التحويل سينتج مستندًا مختلفًا عن الأصلي ولن تكون التوقيعات الرقمية الأصلية صالحة.

هذه المجموعة ليست فارغة أبدا. إذا لم يتم توقيع المستند ، فسيحتوي على صفر من العناصر.

### أمثلة

يوضح كيفية التحقق من صحة المعلومات وعرضها حول كل توقيع في مستند.

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature signature in doc.DigitalSignatures)
{
    Console.WriteLine($"{(signature.IsValid ? "Valid" : "Invalid")} signature: ");
    Console.WriteLine($"\tReason:\t{signature.Comments}"); 
    Console.WriteLine($"\tType:\t{signature.SignatureType}");
    Console.WriteLine($"\tSign time:\t{signature.SignTime}");
    Console.WriteLine($"\tSubject name:\t{signature.CertificateHolder.Certificate.SubjectName}");
    Console.WriteLine($"\tIssuer name:\t{signature.CertificateHolder.Certificate.IssuerName.Name}");
    Console.WriteLine();
}
```

يوضح كيفية توقيع المستندات بشهادات X.509.

```csharp
// تحقق من عدم توقيع المستند.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// أنشئ كائن CertificateHolder من ملف PKCS12 ، والذي سنستخدمه لتوقيع الوثيقة.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// توجد طريقتان لحفظ نسخة موقعة من المستند في نظام الملفات المحلي:
// 1 - قم بتعيين مستند باسم ملف نظام محلي وحفظ نسخة موقعة في موقع محدد بواسطة اسم ملف آخر.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - خذ مستندًا من دفق واحفظ نسخة موقعة في دفق آخر.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// الرجاء التحقق من أن جميع التوقيعات الرقمية الخاصة بالمستند صالحة وتحقق من تفاصيلها.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### أنظر أيضا

* class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


