---
title: SignOptions.Comments
second_title: Aspose.Words für .NET-API-Referenz
description: SignOptions eigendom. Gibt Kommentare zur digitalen Signatur an. Standardwert ist leerer String Empty .
type: docs
weight: 20
url: /de/net/aspose.words.digitalsignatures/signoptions/comments/
---
## SignOptions.Comments property

Gibt Kommentare zur digitalen Signatur an. Standardwert ist **leerer String** (Empty ).

```csharp
public string Comments { get; set; }
```

### Beispiele

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

// Nimm ein unsigniertes Dokument aus dem lokalen Dateisystem über einen Dateistream,
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
* namensraum [Aspose.Words.DigitalSignatures](../../signoptions/)
* Montage [Aspose.Words](../../../)


