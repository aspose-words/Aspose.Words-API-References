---
title: DigitalSignature Class
linktitle: DigitalSignature
articleTitle: DigitalSignature
second_title: Aspose.Words för .NET
description: Aspose.Words.DigitalSignatures.DigitalSignature klass. Representerar en digital signatur på ett dokument och resultatet av dess verifiering i C#.
type: docs
weight: 380
url: /sv/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

Representerar en digital signatur på ett dokument och resultatet av dess verifiering.

För att lära dig mer, besök[Arbeta med digitala signaturer](https://docs.aspose.com/words/net/working-with-digital-signatures/) dokumentationsartikel.

```csharp
public class DigitalSignature
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | Returnerar certifikatinnehavarens objekt som innehåller certifikatet som användes för att signera dokumentet. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | Får kommentaren för signeringssyfte. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | Returnerar subjektets distinguerade namn på certifikatet isuuer. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | Returnerar`Sann` om denna digitala signatur är giltig och dokumentet inte har manipulerats. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | Hämtar typen av digital signatur. |
| [SignatureValue](../../aspose.words.digitalsignatures/digitalsignature/signaturevalue/) { get; } | Får en matris med byte som representerar ett signaturvärde. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | Hämtar tiden då dokumentet signerades. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | Returnerar ämnets unika namn på certifikatet som användes för att signera dokumentet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | Returnerar en användarvänlig sträng som visar värdet på detta objekt. |

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

* namnutrymme [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../)
