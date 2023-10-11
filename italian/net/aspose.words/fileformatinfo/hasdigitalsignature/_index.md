---
title: FileFormatInfo.HasDigitalSignature
second_title: Aspose.Words per .NET API Reference
description: FileFormatInfo proprietà. RestituisceVEROse questo documento contiene una firma digitale. Questa proprietà informa semplicemente che su un documento è presente una firma digitale ma non specifica se la firma è valida o meno.
type: docs
weight: 20
url: /it/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Restituisce`VERO`se questo documento contiene una firma digitale. Questa proprietà informa semplicemente che su un documento è presente una firma digitale, ma non specifica se la firma è valida o meno.

```csharp
public bool HasDigitalSignature { get; }
```

### Osservazioni

Questa proprietà esiste per aiutarti a ordinare i documenti firmati digitalmente da quelli che non lo sono. Se usi Aspose.Words per modificare e salvare un documento firmato digitalmente, la firma digitale andrà persa. Questo è dovuto alla progettazione perché esiste una firma digitale per proteggere l'autenticità di un documento. Usando questa proprietà puoi rilevare i documenti firmati digitalmente prima di elaborarli come normali documenti e intraprendere alcune azioni per evitare di perdere la firma digitale, ad esempio avvisare l'utente.

### Esempi

Mostra come utilizzare la classe FileFormatUtil per rilevare il formato del documento e la presenza di firme digitali.

```csharp
// Utilizzare un'istanza FileFormatInfo per verificare che un documento non sia firmato digitalmente.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// Utilizza una nuova FileFormatInstance per confermare che sia firmata.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Possiamo caricare e accedere alle firme di un documento firmato in una raccolta come questa.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Guarda anche

* class [FileFormatInfo](../)
* spazio dei nomi [Aspose.Words](../../fileformatinfo/)
* assemblea [Aspose.Words](../../../)


