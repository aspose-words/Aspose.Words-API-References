---
title: SignOptions Class
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.DigitalSignatures.SignOptions, um Ihren Dokumentsignaturprozess mit flexiblen und sicheren Optionen für einen verbesserten Arbeitsablauf anzupassen.
type: docs
weight: 620
url: /de/net/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class

Ermöglicht die Angabe von Optionen für die Dokumentsignatur.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public class SignOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [SignOptions](signoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Comments](../../aspose.words.digitalsignatures/signoptions/comments/) { get; set; } | Gibt Kommentare zur digitalen Signatur an. Der Standardwert ist**leere Zeichenfolge**(Empty ). |
| [DecryptionPassword](../../aspose.words.digitalsignatures/signoptions/decryptionpassword/) { get; set; } | Das Passwort zum Entschlüsseln des Quelldokuments. Der Standardwert ist**leere Zeichenfolge** (Empty ). |
| [ProviderId](../../aspose.words.digitalsignatures/signoptions/providerid/) { get; set; } | Gibt die Klassen-ID des Signaturanbieters an. Der Standardwert ist**Leere (nur Nullen) GUID** . |
| [SignatureLineId](../../aspose.words.digitalsignatures/signoptions/signaturelineid/) { get; set; } | Signaturzeilenkennung. Der Standardwert ist**Leere (nur Nullen) GUID** . |
| [SignatureLineImage](../../aspose.words.digitalsignatures/signoptions/signaturelineimage/) { get; set; } | Das Bild, das in den zugehörigen[`SignatureLine`](../../aspose.words.drawing/signatureline/) . Der Standardwert ist`null` . |
| [SignTime](../../aspose.words.digitalsignatures/signoptions/signtime/) { get; set; } | Das Datum der Unterzeichnung. Der Standardwert ist**aktuelle Uhrzeit** (Now) |
| [XmlDsigLevel](../../aspose.words.digitalsignatures/signoptions/xmldsiglevel/) { get; set; } | Gibt die Ebene einer digitalen Signatur basierend auf dem XML-DSig-Standard an. Der Standardwert istXmlDSig . |

## Beispiele

Zeigt, wie Dokumente digital signiert werden.

```csharp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Speicher, das einen privaten Schlüssel enthalten sollte.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie einen Kommentar und ein Datum, die mit unserer neuen digitalen Signatur angewendet werden.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Über einen Dateistream ein unsigniertes Dokument aus dem lokalen Dateisystem holen,
// Erstellen Sie dann eine signierte Kopie davon, die durch den Dateinamen des Ausgabedateistreams bestimmt wird.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Siehe auch

* namensraum [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../)
