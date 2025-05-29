---
title: SignOptions Class
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.DigitalSignatures.SignOptions per personalizzare il processo di firma dei documenti con opzioni flessibili e sicure per un flusso di lavoro ottimizzato.
type: docs
weight: 620
url: /it/net/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class

Consente di specificare le opzioni per la firma del documento.

Per saperne di più, visita il[Lavorare con le firme digitali](https://docs.aspose.com/words/net/working-with-digital-signatures/) articolo di documentazione.

```csharp
public class SignOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [SignOptions](signoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Comments](../../aspose.words.digitalsignatures/signoptions/comments/) { get; set; } | Specifica i commenti sulla firma digitale. Il valore predefinito è**stringa vuota**(Empty ). |
| [DecryptionPassword](../../aspose.words.digitalsignatures/signoptions/decryptionpassword/) { get; set; } | La password per decifrare il documento sorgente. Il valore predefinito è**stringa vuota** (Empty ). |
| [ProviderId](../../aspose.words.digitalsignatures/signoptions/providerid/) { get; set; } | Specifica l'ID di classe del fornitore della firma. Il valore predefinito è**Guid vuoto (tutti zeri)** . |
| [SignatureLineId](../../aspose.words.digitalsignatures/signoptions/signaturelineid/) { get; set; } | Identificatore della riga della firma. Il valore predefinito è**Guid vuoto (tutti zeri)** . |
| [SignatureLineImage](../../aspose.words.digitalsignatures/signoptions/signaturelineimage/) { get; set; } | L'immagine che verrà mostrata in associazione[`SignatureLine`](../../aspose.words.drawing/signatureline/) . Il valore predefinito è`null` . |
| [SignTime](../../aspose.words.digitalsignatures/signoptions/signtime/) { get; set; } | La data della firma. Il valore predefinito è**ora corrente** (Now) |
| [XmlDsigLevel](../../aspose.words.digitalsignatures/signoptions/xmldsiglevel/) { get; set; } | Specifica il livello di una firma digitale basata sullo standard XML-DSig. Il valore predefinito èXmlDSig . |

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

* spazio dei nomi [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../)
