---
title: SignatureLineOptions Class
linktitle: SignatureLineOptions
articleTitle: SignatureLineOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.SignatureLineOptions per personalizzare facilmente le righe della firma nei tuoi documenti. Migliora la tua esperienza con DocumentBuilder oggi stesso!
type: docs
weight: 6940
url: /it/net/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class

Consente di specificare le opzioni per l'inserimento della riga della firma. Utilizzato in[`DocumentBuilder`](../documentbuilder/) .

Per saperne di più, visita il[Lavorare con le firme digitali](https://docs.aspose.com/words/net/working-with-digital-signatures/) articolo di documentazione.

```csharp
public class SignatureLineOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [SignatureLineOptions](signaturelineoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowComments](../../aspose.words/signaturelineoptions/allowcomments/) { get; set; } | Ottiene o imposta un valore che indica che il firmatario può aggiungere commenti nella finestra di dialogo Firma. Il valore predefinito per questa proprietà è`falso` . |
| [DefaultInstructions](../../aspose.words/signaturelineoptions/defaultinstructions/) { get; set; } | Ottiene o imposta un valore che indica che le istruzioni predefinite vengono visualizzate nella finestra di dialogo Segno. Il valore predefinito per questa proprietà è`VERO` . |
| [Email](../../aspose.words/signaturelineoptions/email/) { get; set; } | Ottiene o imposta l'indirizzo e-mail del firmatario suggerito. Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |
| [Instructions](../../aspose.words/signaturelineoptions/instructions/) { get; set; } | Ottiene o imposta le istruzioni per il firmatario che vengono visualizzate quando si firma la riga della firma. Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |
| [ShowDate](../../aspose.words/signaturelineoptions/showdate/) { get; set; } | Ottiene o imposta un valore che indica che la data della firma è visualizzata nella riga della firma. Il valore predefinito per questa proprietà è`VERO` . |
| [Signer](../../aspose.words/signaturelineoptions/signer/) { get; set; } | Ottiene o imposta il firmatario suggerito della riga della firma. Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |
| [SignerTitle](../../aspose.words/signaturelineoptions/signertitle/) { get; set; } | Ottiene o imposta il titolo suggerito del firmatario. Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
