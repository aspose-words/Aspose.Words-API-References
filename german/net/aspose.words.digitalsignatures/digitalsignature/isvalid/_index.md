---
title: DigitalSignature.IsValid
second_title: Aspose.Words für .NET-API-Referenz
description: DigitalSignature eigendom. Gibt zurückWAHR wenn diese digitale Signatur gültig ist und das Dokument nicht manipuliert wurde.
type: docs
weight: 40
url: /de/net/aspose.words.digitalsignatures/digitalsignature/isvalid/
---
## DigitalSignature.IsValid property

Gibt zurück`WAHR` wenn diese digitale Signatur gültig ist und das Dokument nicht manipuliert wurde.

```csharp
public bool IsValid { get; }
```

### Beispiele

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
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* Montage [Aspose.Words](../../../)


