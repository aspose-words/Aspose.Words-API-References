---
title: DigitalSignature.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words für .NET
description: Entdecken Sie die DigitalSignature-Kommentare-Funktion, um Ihren Signaturprozess mit klaren Zweckkommentaren zu verbessern. Steigern Sie die Effizienz und Übersichtlichkeit Ihrer Dokumente!
type: docs
weight: 20
url: /de/net/aspose.words.digitalsignatures/digitalsignature/comments/
---
## DigitalSignature.Comments property

Ruft den Kommentar zum Signierungszweck ab.

```csharp
public string Comments { get; }
```

## Beispiele

Zeigt, wie Informationen zu jeder Signatur in einem Dokument validiert und angezeigt werden.

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

### Siehe auch

* class [DigitalSignature](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
