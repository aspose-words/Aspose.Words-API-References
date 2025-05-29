---
title: DigitalSignature.IssuerName
linktitle: IssuerName
articleTitle: IssuerName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية DigitalSignature IssuerName، التي توفر الاسم المميز للجهة المصدرة لتحسين الأمان والثقة في شهاداتك الرقمية.
type: docs
weight: 30
url: /ar/net/aspose.words.digitalsignatures/digitalsignature/issuername/
---
## DigitalSignature.IssuerName property

يعيد اسم الموضوع المميز لمصدر الشهادة.

```csharp
public string IssuerName { get; }
```

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

* class [DigitalSignature](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
