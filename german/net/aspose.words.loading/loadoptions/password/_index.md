---
title: LoadOptions.Password
second_title: Aspose.Words für .NET-API-Referenz
description: LoadOptions eigendom. Ruft das Passwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann seinNull oder leere Zeichenfolge. Standard istNull .
type: docs
weight: 110
url: /de/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Ruft das Passwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann sein`Null` oder leere Zeichenfolge. Standard ist`Null` .

```csharp
public string Password { get; set; }
```

### Bemerkungen

Sie müssen das Passwort kennen, um ein verschlüsseltes Dokument zu öffnen. Wenn das Dokument nicht verschlüsselt ist, stellen Sie dies auf ein`Null` oder leere Zeichenfolge.

### Beispiele

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

// Legen Sie einen lokalen Systemdateinamen für das unsignierte Eingabedokument und einen Ausgabedateinamen für seine neue digital signierte Kopie fest.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)


