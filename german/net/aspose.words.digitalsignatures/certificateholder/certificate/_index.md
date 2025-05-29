---
title: CertificateHolder.Certificate
linktitle: Certificate
articleTitle: Certificate
second_title: Aspose.Words für .NET
description: Greifen Sie mit privaten Schlüsseln und Zertifikatskette auf die X509Certificate2-Instanz zu. Vereinfachen Sie Ihr Sicherheitsmanagement mit unserer CertificateHolder-Eigenschaft.
type: docs
weight: 20
url: /de/net/aspose.words.digitalsignatures/certificateholder/certificate/
---
## CertificateHolder.Certificate property

Gibt die Instanz von**X509Zertifikat2** die private und öffentliche Schlüssel sowie die Zertifikatskette enthält.

```csharp
public X509Certificate2 Certificate { get; }
```

### Rückgabewert

X509Certificate2 Beispiel

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

* class [CertificateHolder](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
