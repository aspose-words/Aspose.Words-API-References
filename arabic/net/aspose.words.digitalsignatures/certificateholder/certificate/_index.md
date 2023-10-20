---
title: CertificateHolder.Certificate
linktitle: Certificate
articleTitle: Certificate
second_title: Aspose.Words لـ .NET
description: CertificateHolder Certificate ملكية. إرجاع مثيلشهادة X5092 الذي يحمل المفاتيح الخاصة والعامة وسلسلة الشهادات في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.digitalsignatures/certificateholder/certificate/
---
## CertificateHolder.Certificate property

إرجاع مثيل**شهادة X5092** الذي يحمل المفاتيح الخاصة والعامة وسلسلة الشهادات.

```csharp
public X509Certificate2 Certificate { get; }
```

### قيمة الإرجاع

X509Certificate2 مثال

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

* class [CertificateHolder](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
