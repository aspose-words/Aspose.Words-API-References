---
title: Document.DigitalSignatures
linktitle: DigitalSignatures
articleTitle: DigitalSignatures
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية DigitalSignatures للوصول إلى التوقيعات الرقمية للمستندات والتحقق منها بسهولة. اضمن مصداقيتها وأمانها بسهولة.
type: docs
weight: 110
url: /ar/net/aspose.words/document/digitalsignatures/
---
## Document.DigitalSignatures property

يحصل على مجموعة التوقيعات الرقمية لهذه الوثيقة ونتائج التحقق منها.

```csharp
public DigitalSignatureCollection DigitalSignatures { get; }
```

## ملاحظات

تحتوي هذه المجموعة على توقيعات رقمية تم تحميلها من المستند الأصلي. لن يتم حفظ هذه التوقيعات الرقمية عند حفظ هذا[`Document`](../) object في ملف أو مجرى لأن الحفظ أو التحويل سيؤدي إلى إنشاء مستند مختلف عن المستند الأصلي ولن تكون التوقيعات الرقمية الأصلية صالحة بعد الآن.

هذه المجموعة ليست أبدًا`باطل`إذا لم يتم توقيع المستند، فسوف يحتوي على صفر من العناصر.

## أمثلة

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

* class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
