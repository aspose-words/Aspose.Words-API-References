---
title: DigitalSignatureCollection Class
linktitle: DigitalSignatureCollection
articleTitle: DigitalSignatureCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words DigitalSignatureCollection، التي توفر سهولة الوصول إلى مجموعة للقراءة فقط من التوقيعات الرقمية لإدارة المستندات بشكل آمن.
type: docs
weight: 590
url: /ar/net/aspose.words.digitalsignatures/digitalsignaturecollection/
---
## DigitalSignatureCollection class

يوفر مجموعة للقراءة فقط من التوقيعات الرقمية المرفقة بمستند.

لمعرفة المزيد، قم بزيارة[العمل مع التوقيعات الرقمية](https://docs.aspose.com/words/net/working-with-digital-signatures/) مقالة توثيقية.

```csharp
public class DigitalSignatureCollection : IEnumerable<DigitalSignature>
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [DigitalSignatureCollection](digitalsignaturecollection/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.digitalsignatures/digitalsignaturecollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/) { get; } | إرجاع`حقيقي`إذا كانت جميع التوقيعات الرقمية في هذه المجموعة صالحة ولم يتم العبث بالمستند ، فسيتم أيضًا إرجاع`حقيقي` إذا لم تكن هناك توقيعات رقمية. يعود`خطأ شنيع` إذا كان هناك على الأقل توقيع رقمي واحد غير صالح. |
| [Item](../../aspose.words.digitalsignatures/digitalsignaturecollection/item/) { get; } | يحصل على توقيع مستند في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/)() | يعيد كائن عداد القاموس الذي يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |

## ملاحظات

[`DigitalSignatures`](../../aspose.words/document/digitalsignatures/)

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

* class [DigitalSignature](../digitalsignature/)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../)
