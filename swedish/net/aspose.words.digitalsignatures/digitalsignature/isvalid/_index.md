---
title: DigitalSignature.IsValid
linktitle: IsValid
articleTitle: IsValid
second_title: Aspose.Words för .NET
description: Säkerställ dokumentintegritet med egenskapen DigitalSignature IsValid, vilket bekräftar äkthet och skyddar mot manipulering. Lita på dina digitala signaturer!
type: docs
weight: 40
url: /sv/net/aspose.words.digitalsignatures/digitalsignature/isvalid/
---
## DigitalSignature.IsValid property

Returer`sann` om denna digitala signatur är giltig och dokumentet inte har manipulerats.

```csharp
public bool IsValid { get; }
```

## Exempel

Visar hur man validerar och visar information om varje signatur i ett dokument.

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

### Se även

* class [DigitalSignature](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
