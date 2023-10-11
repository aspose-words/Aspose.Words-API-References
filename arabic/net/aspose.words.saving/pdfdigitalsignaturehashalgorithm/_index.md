---
title: Enum PdfDigitalSignatureHashAlgorithm
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.PdfDigitalSignatureHashAlgorithm تعداد. يحدد خوارزمية التجزئة الرقمية المستخدمة بواسطة التوقيع الرقمي.
type: docs
weight: 5440
url: /ar/net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---
## PdfDigitalSignatureHashAlgorithm enumeration

يحدد خوارزمية التجزئة الرقمية المستخدمة بواسطة التوقيع الرقمي.

```csharp
public enum PdfDigitalSignatureHashAlgorithm
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Sha256 | `0` | خوارزمية التجزئة SHA-256. |
| Sha384 | `1` | خوارزمية التجزئة SHA-384. |
| Sha512 | `2` | خوارزمية التجزئة SHA-512. |
| RipeMD160 | `3` | خوارزمية التجزئة RIPEMD-160. |

### أمثلة

يوضح كيفية التوقيع على مستند PDF تم إنشاؤه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتكوين كائن "DigitalSignatureDetails" للكائن "SaveOptions" إلى
// قم بتوقيع المستند رقميًا أثناء عرضه باستخدام طريقة "الحفظ".
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


