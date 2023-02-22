---
title: DigitalSignature.IsValid
second_title: Aspose.Words لمراجع .NET API
description: DigitalSignature ملكية. يعود صحيحًا إذا كان هذا التوقيع الرقمي صحيحًا ولم يتم العبث بالمستند.
type: docs
weight: 40
url: /ar/net/aspose.words.digitalsignatures/digitalsignature/isvalid/
---
## DigitalSignature.IsValid property

يعود صحيحًا إذا كان هذا التوقيع الرقمي صحيحًا ولم يتم العبث بالمستند.

```csharp
public bool IsValid { get; }
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


