---
title: Class DigitalSignature
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.DigitalSignatures.DigitalSignature فصل. يمثل توقيعًا رقميًا على مستند ونتيجة التحقق منه.
type: docs
weight: 370
url: /ar/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

يمثل توقيعًا رقميًا على مستند ونتيجة التحقق منه.

```csharp
public class DigitalSignature
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | إرجاع كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | الحصول على تعليق غرض التوقيع. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | إرجاع الاسم المميز للموضوع للشهادة isuuer. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | يعود صحيحًا إذا كان هذا التوقيع الرقمي صحيحًا ولم يتم العبث بالمستند. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | يحصل على نوع التوقيع الرقمي. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | يحصل على الوقت الذي تم فيه توقيع المستند. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | إرجاع الاسم المميز للموضوع للشهادة التي تم استخدامها لتوقيع المستند. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | إرجاع سلسلة سهلة الاستخدام تعرض قيمة هذا الكائن. |

### أمثلة

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


