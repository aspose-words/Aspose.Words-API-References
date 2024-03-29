---
title: DigitalSignatureCollection.IsValid
linktitle: IsValid
articleTitle: IsValid
second_title: Aspose.Words لـ .NET
description: DigitalSignatureCollection IsValid ملكية. إرجاعحقيقي إذا كانت كافة التوقيعات الرقمية في هذه المجموعة صالحة ولم يتم التلاعب بالمستند بـ فسيتم إرجاعه أيضًاحقيقي إذا لم يكن هناك توقيعات رقمية. يعودخطأ شنيع إذا كان هناك توقيع رقمي واحد على الأقل غير صالح في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/
---
## DigitalSignatureCollection.IsValid property

إرجاع`حقيقي` إذا كانت كافة التوقيعات الرقمية في هذه المجموعة صالحة ولم يتم التلاعب بالمستند بـ فسيتم إرجاعه أيضًا`حقيقي` إذا لم يكن هناك توقيعات رقمية. يعود`خطأ شنيع` إذا كان هناك توقيع رقمي واحد على الأقل غير صالح.

```csharp
public bool IsValid { get; }
```

## أمثلة

يوضح كيفية توقيع المستندات بشهادات X.509.

```csharp
// التحقق من عدم توقيع المستند.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// أنشئ كائن حامل الشهادة من ملف PKCS12، والذي سنستخدمه لتوقيع المستند.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// هناك طريقتان لحفظ نسخة موقعة من المستند في نظام الملفات المحلي:
// 1 - قم بتعيين مستند باسم ملف نظام محلي واحفظ نسخة موقعة في موقع محدد بواسطة اسم ملف آخر.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - خذ مستندًا من الدفق واحفظ نسخة موقعة في دفق آخر.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// يرجى التحقق من صحة جميع التوقيعات الرقمية للمستند والتحقق من تفاصيلها.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### أنظر أيضا

* class [DigitalSignatureCollection](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
