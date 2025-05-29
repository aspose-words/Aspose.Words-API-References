---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre verschlüsselten Dokumente mühelos mit der LoadOptions-Passwortfunktion. Legen Sie Ihr Passwort sicher fest oder rufen Sie es für einen reibungslosen Zugriff ab.
type: docs
weight: 110
url: /de/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Ruft das Kennwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann`null` oder leere Zeichenfolge. Standard ist`null` .

```csharp
public string Password { get; set; }
```

## Bemerkungen

Sie benötigen das Passwort, um ein verschlüsseltes Dokument zu öffnen. Wenn das Dokument nicht verschlüsselt ist, setzen Sie es auf`null` oder eine leere Zeichenfolge.

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

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
