---
title: SignOptions.SignTime
second_title: Aspose.Words per .NET API Reference
description: SignOptions proprietà. La data della firma. Il valore predefinito è ora attuale Now.
type: docs
weight: 70
url: /it/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

La data della firma. Il valore predefinito è **ora attuale** (Now).

```csharp
public DateTime SignTime { get; set; }
```

### Esempi

Mostra come firmare digitalmente i documenti.

```csharp
// Crea un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un commento e una data che verranno applicati con la nostra nuova firma digitale.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Preleva un documento non firmato dal file system locale tramite un flusso di file,
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
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../signoptions/)
* assemblea [Aspose.Words](../../../)


