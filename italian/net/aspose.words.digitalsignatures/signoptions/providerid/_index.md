---
title: SignOptions.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words per .NET
description: Scopri la proprietà ProviderId di SignOptions, che definisce l'ID di classe del tuo provider di firme. Personalizzala facilmente con un GUID univoco per prestazioni ottimali.
type: docs
weight: 40
url: /it/net/aspose.words.digitalsignatures/signoptions/providerid/
---
## SignOptions.ProviderId property

Specifica l'ID di classe del fornitore della firma. Il valore predefinito è**Guid vuoto (tutti zeri)** .

```csharp
public Guid ProviderId { get; set; }
```

## Osservazioni

Il fornitore di servizi crittografici (CSP) è un modulo software indipendente che esegue effettivamente algoritmi di crittografia per l'autenticazione, la codifica e la crittografia. MS Office riserva il valore di {00000000-0000-0000-0000-000000000000} per il suo fornitore di firme predefinito.

Il GUID del provider installato in aggiunta dovrebbe essere ricavato dalla documentazione fornita con il provider.

Inoltre, tutti i provider crittografici installati sono elencati nel registro di Windows. È possibile trovarli nel seguente percorso: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Esiste un nome chiave "CP Service UUID" che corrisponde al GUID del provider della firma.

## Esempi

Mostra come firmare un documento con un certificato personale e una riga per la firma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Riapri il nostro documento salvato e verifica che le proprietà "IsSigned" e "IsValid" siano entrambe uguali a "true",
// indica che la riga della firma contiene una firma.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Guarda anche

* class [SignOptions](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
