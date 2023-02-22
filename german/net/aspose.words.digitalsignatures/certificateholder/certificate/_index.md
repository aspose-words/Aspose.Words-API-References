---
title: CertificateHolder.Certificate
second_title: Aspose.Words für .NET-API-Referenz
description: CertificateHolder eigendom. Gibt die Instanz von zurück X509Zertifikat2 die private öffentliche Schlüssel und Zertifikatskette enthält.
type: docs
weight: 20
url: /de/net/aspose.words.digitalsignatures/certificateholder/certificate/
---
## CertificateHolder.Certificate property

Gibt die Instanz von zurück **X509Zertifikat2** die private, öffentliche Schlüssel und Zertifikatskette enthält.

```csharp
public X509Certificate2 Certificate { get; }
```

### Rückgabewert

X509Certificate2 Beispiel

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

* class [CertificateHolder](../)
* namensraum [Aspose.Words.DigitalSignatures](../../certificateholder/)
* Montage [Aspose.Words](../../../)


