---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words per .NET
description: Scopri la proprietà FileFormatInfo HasDigitalSignature controlla rapidamente se il tuo documento include una firma digitale, migliorando sicurezza e autenticità.
type: docs
weight: 20
url: /it/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Restituisce`VERO`se questo documento contiene una firma digitale. Questa proprietà informa semplicemente che una firma digitale è presente su un documento, ma non specifica se la firma è valida o meno.

```csharp
public bool HasDigitalSignature { get; }
```

## Osservazioni

Questa proprietà esiste per aiutarti a distinguere i documenti firmati digitalmente da quelli che non lo sono. Se utilizzi Aspose.Words per modificare e salvare un documento firmato digitalmente, la firma digitale andrà persa. Questo è intenzionale, perché la firma digitale esiste per salvaguardare l'autenticità di un documento. Utilizzando questa proprietà puoi rilevare i documenti firmati digitalmente prima di elaborarli come documenti normali e intraprendere azioni per evitare di perderla, ad esempio inviare una notifica all'utente.

## Esempi

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato del documento e la presenza di firme digitali.

```csharp
// Utilizzare un'istanza di FileFormatInfo per verificare che un documento non sia firmato digitalmente.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// Utilizzare un nuovo FileFormatInstance per confermare che è firmato.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Possiamo caricare e accedere alle firme di un documento firmato in una raccolta come questa.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Guarda anche

* class [FileFormatInfo](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
