---
title: CertificateHolder.Certificate
linktitle: Certificate
articleTitle: Certificate
second_title: Aspose.Words för .NET
description: Få åtkomst till X509Certificate2-instansen med privata nycklar och certifikatkedja. Förenkla din säkerhetshantering med vår CertificateHolder-egenskap.
type: docs
weight: 20
url: /sv/net/aspose.words.digitalsignatures/certificateholder/certificate/
---
## CertificateHolder.Certificate property

Returnerar instansen av**X509Certifikat2** som innehåller privata, publika nycklar och certifikatkedja.

```csharp
public X509Certificate2 Certificate { get; }
```

### Returvärde

X509Certificate2 exempel

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

* class [CertificateHolder](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
