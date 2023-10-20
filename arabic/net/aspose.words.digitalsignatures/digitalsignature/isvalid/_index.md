---
title: DigitalSignature.IsValid
linktitle: IsValid
articleTitle: IsValid
second_title: Aspose.Words لـ .NET
description: DigitalSignature IsValid ملكية. إرجاعحقيقي إذا كان هذا التوقيع الرقمي صالحًا ولم يتم العبث بالمستند في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.digitalsignatures/digitalsignature/isvalid/
---
## DigitalSignature.IsValid property

إرجاع`حقيقي` إذا كان هذا التوقيع الرقمي صالحًا ولم يتم العبث بالمستند.

```csharp
public bool IsValid { get; }
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

* class [DigitalSignature](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
