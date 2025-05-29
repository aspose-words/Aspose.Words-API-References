---
title: DigitalSignature Class
linktitle: DigitalSignature
articleTitle: DigitalSignature
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.DigitalSignatures.DigitalSignature für sicheres Signieren und Verifizieren von Dokumenten. Verbessern Sie mühelos die Sicherheit Ihrer Dokumente!
type: docs
weight: 580
url: /de/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

Stellt eine digitale Signatur auf einem Dokument und das Ergebnis ihrer Überprüfung dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public class DigitalSignature
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | Gibt das Zertifikatsinhaberobjekt zurück, das das zum Signieren des Dokuments verwendete Zertifikat enthält. |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | Ruft den Kommentar zum Signierungszweck ab. |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | Gibt den Distinguished Name des Zertifikatsausstellers zurück. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | Rückgaben`WAHR` ob diese digitale Signatur gültig ist und das Dokument nicht manipuliert wurde. |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | Ruft den Typ der digitalen Signatur ab. |
| [SignatureValue](../../aspose.words.digitalsignatures/digitalsignature/signaturevalue/) { get; } | Ruft ein Byte-Array ab, das einen Signaturwert darstellt. |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | Ruft den Zeitpunkt ab, zu dem das Dokument signiert wurde. |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | Gibt den eindeutigen Betreff des Zertifikats zurück, das zum Signieren des Dokuments verwendet wurde. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | Gibt eine benutzerfreundliche Zeichenfolge zurück, die den Wert dieses Objekts anzeigt. |

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

* namensraum [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../)
