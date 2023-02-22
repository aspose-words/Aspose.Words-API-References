---
title: DigitalSignature.Comments
second_title: Aspose.Words لمراجع .NET API
description: DigitalSignature ملكية. الحصول على تعليق غرض التوقيع.
type: docs
weight: 20
url: /ar/net/aspose.words.digitalsignatures/digitalsignature/comments/
---
## DigitalSignature.Comments property

الحصول على تعليق غرض التوقيع.

```csharp
public string Comments { get; }
```

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

* class [DigitalSignature](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* المجسم [Aspose.Words](../../../)


