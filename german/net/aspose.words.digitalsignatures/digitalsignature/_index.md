---
title: Class DigitalSignature
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.DigitalSignatures.DigitalSignature klas. Stellt eine digitale Signatur auf einem Dokument und das Ergebnis seiner Überprüfung dar.
type: docs
weight: 370
url: /de/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

Stellt eine digitale Signatur auf einem Dokument und das Ergebnis seiner Überprüfung dar.

```csharp
public class DigitalSignature
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | Gibt das Zertifikatsinhaberobjekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | Ruft den Kommentar zum Signierungszweck ab. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | Gibt den Distinguished Name des Zertifikatsausstellers zurück. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | Gibt wahr zurück, wenn diese digitale Signatur gültig ist und das Dokument nicht manipuliert wurde. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | Ruft den Typ der digitalen Signatur ab. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | Ruft die Zeit ab, zu der das Dokument signiert wurde. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | Gibt den Distinguished Name des Zertifikats zurück, das zum Signieren des Dokuments verwendet wurde. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | Gibt eine benutzerfreundliche Zeichenfolge zurück, die den Wert dieses Objekts anzeigt. |

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

* namensraum [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../)


