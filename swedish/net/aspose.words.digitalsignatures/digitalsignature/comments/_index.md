---
title: DigitalSignature.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Kommentarer till digitala signaturer för att förbättra din signeringsprocess med tydliga kommentarer. Öka effektiviteten och tydligheten i dina dokument.
type: docs
weight: 20
url: /sv/net/aspose.words.digitalsignatures/digitalsignature/comments/
---
## DigitalSignature.Comments property

Hämtar kommentaren om signeringssyftet.

```csharp
public string Comments { get; }
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
