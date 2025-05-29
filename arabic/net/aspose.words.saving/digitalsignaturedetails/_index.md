---
title: DigitalSignatureDetails Class
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.DigitalSignatureDetails لتوقيع مستندات رقمية سلس. حسّن الأمان والمصداقية بسهولة!
type: docs
weight: 5640
url: /ar/net/aspose.words.saving/digitalsignaturedetails/
---
## DigitalSignatureDetails class

يحتوي على تفاصيل حول توقيع مستند باستخدام توقيع رقمي.

```csharp
public class DigitalSignatureDetails
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [DigitalSignatureDetails](digitalsignaturedetails/)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), [SignOptions](../../aspose.words.digitalsignatures/signoptions/)*) | يقوم بتهيئة مثيل جديد لـ`DigitalSignatureDetails` الصف. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/digitalsignaturedetails/certificateholder/) { get; set; } | يحصل على أو يعين[`CertificateHolder`](./certificateholder/) الكائن الذي يحتوي على الشهادة المستخدمة لتوقيع مستند. |
| [SignOptions](../../aspose.words.saving/digitalsignaturedetails/signoptions/) { get; set; } | يحصل على أو يعين[`SignOptions`](./signoptions/) الكائن المستخدم لتوقيع مستند. |

## أمثلة

يوضح كيفية توقيع مستند OOXML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
DigitalSignatureDetails digitalSignatureDetails = new DigitalSignatureDetails(
    certificateHolder,
    new SignOptions() { Comments = "Some comments", SignTime = DateTime.Now });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.DigitalSignatureDetails = digitalSignatureDetails;

Assert.AreEqual(certificateHolder, digitalSignatureDetails.CertificateHolder);
Assert.AreEqual("Some comments", digitalSignatureDetails.SignOptions.Comments);

doc.Save(ArtifactsDir + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
