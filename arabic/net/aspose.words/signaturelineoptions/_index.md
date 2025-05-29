---
title: SignatureLineOptions Class
linktitle: SignatureLineOptions
articleTitle: SignatureLineOptions
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.SignatureLineOptions لتخصيص أسطر التوقيع في مستنداتك بسهولة. حسّن تجربة DocumentBuilder اليوم!
type: docs
weight: 6940
url: /ar/net/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class

يسمح بتحديد خيارات لإدراج سطر التوقيع. يُستخدم في[`DocumentBuilder`](../documentbuilder/) .

لمعرفة المزيد، قم بزيارة[العمل مع التوقيعات الرقمية](https://docs.aspose.com/words/net/working-with-digital-signatures/) مقالة توثيقية.

```csharp
public class SignatureLineOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [SignatureLineOptions](signaturelineoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowComments](../../aspose.words/signaturelineoptions/allowcomments/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى أن المُوقِّع يمكنه إضافة تعليقات في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [DefaultInstructions](../../aspose.words/signaturelineoptions/defaultinstructions/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى أن التعليمات الافتراضية تظهر في مربع الحوار "التوقيع". القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [Email](../../aspose.words/signaturelineoptions/email/) { get; set; } | يحصل على عنوان البريد الإلكتروني للموقع المقترح أو يعينه. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [Instructions](../../aspose.words/signaturelineoptions/instructions/) { get; set; } | يحصل على التعليمات أو يعينها للموقع والتي يتم عرضها عند توقيع سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [ShowDate](../../aspose.words/signaturelineoptions/showdate/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى أن تاريخ التوقيع يظهر في سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [Signer](../../aspose.words/signaturelineoptions/signer/) { get; set; } | يحصل على أو يعين الموقع المقترح لسطر التوقيع. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [SignerTitle](../../aspose.words/signaturelineoptions/signertitle/) { get; set; } | يحصل على عنوان المُوقِّع المُقترح أو يُعيِّنه. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |

## أمثلة

يوضح كيفية توقيع مستند باستخدام شهادة شخصية وسطر التوقيع.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// أعد فتح المستند المحفوظ لدينا، وتأكد من أن الخاصيتين "IsSigned" و"IsValid" تساويان "true"،
// يشير إلى أن سطر التوقيع يحتوي على توقيع.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
