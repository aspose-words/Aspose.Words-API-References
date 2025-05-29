---
title: DigitalSignatureDetails.CertificateHolder
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية حامل شهادة DigitalSignatureDetails لإدارة شهادة توقيع مستندك بسهولة. حسّن الأمان وسهّل العمليات!
type: docs
weight: 20
url: /ar/net/aspose.words.saving/digitalsignaturedetails/certificateholder/
---
## DigitalSignatureDetails.CertificateHolder property

يحصل على أو يعين`CertificateHolder` الكائن الذي يحتوي على الشهادة المستخدمة لتوقيع مستند.

```csharp
public CertificateHolder CertificateHolder { get; set; }
```

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

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [DigitalSignatureDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
