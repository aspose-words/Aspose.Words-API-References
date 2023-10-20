---
title: SignOptions.SignTime
linktitle: SignTime
articleTitle: SignTime
second_title: Aspose.Words für .NET
description: SignOptions SignTime eigendom. Das Datum der Unterzeichnung. Der Standardwert istaktuelle Uhrzeit Now in C#.
type: docs
weight: 70
url: /de/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

Das Datum der Unterzeichnung. Der Standardwert ist**aktuelle Uhrzeit** (Now).

```csharp
public DateTime SignTime { get; set; }
```

## Beispiele

Zeigt, wie man Dokumente digital signiert.

```csharp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Speicher, das einen privaten Schlüssel enthalten sollte.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie einen Kommentar und ein Datum, das mit unserer neuen digitalen Signatur angewendet wird.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Über einen Dateistream ein unsigniertes Dokument aus dem lokalen Dateisystem übernehmen,
// dann eine signierte Kopie davon erstellen, die durch den Dateinamen des Ausgabedateistreams bestimmt wird.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Siehe auch

* class [SignOptions](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
