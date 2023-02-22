---
title: Enum DigitalSignatureType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.DigitalSignatures.DigitalSignatureType تعداد. يحدد نوع التوقيع الرقمي.
type: docs
weight: 390
url: /ar/net/aspose.words.digitalsignatures/digitalsignaturetype/
---
## DigitalSignatureType enumeration

يحدد نوع التوقيع الرقمي.

```csharp
public enum DigitalSignatureType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Unknown | `0` | يشير إلى خطأ ، نوع التوقيع الرقمي غير معروف. |
| CryptoApi | `1` | طريقة توقيع Crypto API المستخدمة في مستندات Microsoft Word 97-2003 الثنائية .DOC. |
| XmlDsig | `2` | طريقة التوقيع XmlDsig المستخدمة في مستندات OOXML و OpenDocument. |

### أمثلة

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

* مساحة الاسم [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../)


