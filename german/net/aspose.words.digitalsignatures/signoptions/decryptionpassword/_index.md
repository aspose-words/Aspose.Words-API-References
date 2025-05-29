---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: Aspose.Words für .NET
description: Entsperren Sie Ihre Dokumente mühelos mit der DecryptionPassword-Funktion von SignOptions. Entschlüsseln Sie Quelldateien sicher und einfach; der Standardwert ist eine leere Zeichenfolge.
type: docs
weight: 30
url: /de/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

Das Passwort zum Entschlüsseln des Quelldokuments. Der Standardwert ist**leere Zeichenfolge** (Empty ).

```csharp
public string DecryptionPassword { get; set; }
```

## Bemerkungen

Wenn das OOXML-Dokument verschlüsselt ist, müssen Sie ein Entschlüsselungskennwort angeben, um das Quelldokument zu entschlüsseln, bevor es signiert wird. Dies ist für Dokumente im binären DOC-Format nicht erforderlich.

## Beispiele

Zeigt, wie eine verschlüsselte Dokumentdatei signiert wird.

```csharp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Speicher, das einen privaten Schlüssel enthalten sollte.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie einen Kommentar, ein Datum und ein Entschlüsselungskennwort, das mit unserer neuen digitalen Signatur angewendet wird.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Legen Sie einen lokalen Systemdateinamen für das unsignierte Eingabedokument und einen Ausgabedateinamen für die neue digital signierte Kopie fest.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Siehe auch

* class [SignOptions](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
