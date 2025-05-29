---
title: SignOptions.SignTime
linktitle: SignTime
articleTitle: SignTime
second_title: Aspose.Words für .NET
description: Entdecken Sie SignOptions SignTime für müheloses Signieren. Stellen Sie das Signierungsdatum einfach auf die aktuelle Uhrzeit ein. Optimieren Sie Ihren Dokumentenprozess!
type: docs
weight: 70
url: /de/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

Das Datum der Unterzeichnung. Der Standardwert ist**aktuelle Uhrzeit** (Now)

```csharp
public DateTime SignTime { get; set; }
```

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

* class [SignOptions](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
