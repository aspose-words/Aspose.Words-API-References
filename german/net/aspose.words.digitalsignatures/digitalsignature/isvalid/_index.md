---
title: DigitalSignature.IsValid
linktitle: IsValid
articleTitle: IsValid
second_title: Aspose.Words für .NET
description: Stellen Sie die Dokumentintegrität mit der Eigenschaft „DigitalSignature IsValid“ sicher, die Authentizität bestätigt und vor Manipulation schützt. Vertrauen Sie Ihren digitalen Signaturen!
type: docs
weight: 40
url: /de/net/aspose.words.digitalsignatures/digitalsignature/isvalid/
---
## DigitalSignature.IsValid property

Rückgaben`WAHR` ob diese digitale Signatur gültig ist und das Dokument nicht manipuliert wurde.

```csharp
public bool IsValid { get; }
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
