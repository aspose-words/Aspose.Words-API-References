---
title: DigitalSignature.SignatureType
linktitle: SignatureType
articleTitle: SignatureType
second_title: Aspose.Words لـ .NET
description: DigitalSignature SignatureType ملكية. الحصول على نوع التوقيع الرقمي في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.digitalsignatures/digitalsignature/signaturetype/
---
## DigitalSignature.SignatureType property

الحصول على نوع التوقيع الرقمي.

```csharp
public DigitalSignatureType SignatureType { get; }
```

## أمثلة

يوضح كيفية التحقق من صحة وعرض المعلومات حول كل توقيع في المستند.

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

* enum [DigitalSignatureType](../../digitalsignaturetype/)
* class [DigitalSignature](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
