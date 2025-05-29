---
title: SignOptions.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words per .NET
description: Scopri la proprietà Commenti di SignOptions per migliorare la tua firma digitale con note personalizzate. Migliora la chiarezza e la comunicazione senza sforzo!
type: docs
weight: 20
url: /it/net/aspose.words.digitalsignatures/signoptions/comments/
---
## SignOptions.Comments property

Specifica i commenti sulla firma digitale. Il valore predefinito è**stringa vuota**(Empty ).

```csharp
public string Comments { get; set; }
```

## Esempi

Mostra come firmare digitalmente i documenti.

```csharp
// Creare un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un commento e una data che verranno applicati con la nostra nuova firma digitale.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Prendi un documento non firmato dal file system locale tramite un flusso di file,
// quindi crea una copia firmata determinata dal nome file del flusso di file di output.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Guarda anche

* class [SignOptions](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
