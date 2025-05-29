---
title: DigitalSignature Class
linktitle: DigitalSignature
articleTitle: DigitalSignature
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.DigitalSignatures.DigitalSignature لتوقيع المستندات والتحقق منها بأمان. عزز أمان مستنداتك بسهولة!
type: docs
weight: 580
url: /ar/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

يمثل التوقيع الرقمي على مستند ونتيجة التحقق منه.

لمعرفة المزيد، قم بزيارة[العمل مع التوقيعات الرقمية](https://docs.aspose.com/words/net/working-with-digital-signatures/) مقالة توثيقية.

```csharp
public class DigitalSignature
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | يعيد كائن حامل الشهادة الذي يحتوي على الشهادة التي تم استخدامها لتوقيع المستند. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | يحصل على تعليق غرض التوقيع. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | يعيد اسم الموضوع المميز لمصدر الشهادة. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | إرجاع`حقيقي` إذا كان هذا التوقيع الرقمي صالحًا ولم يتم العبث بالمستند. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | يحصل على نوع التوقيع الرقمي. |
| [SignatureValue](../../aspose.words.digitalsignatures/digitalsignature/signaturevalue/) { get; } | يحصل على مجموعة من البايتات التي تمثل قيمة التوقيع. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | يحصل على الوقت الذي تم فيه توقيع المستند. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | يعيد اسم الموضوع المميز للشهادة التي تم استخدامها لتوقيع المستند. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | يعيد سلسلة سهلة الاستخدام تعرض قيمة هذا الكائن. |

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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../)
