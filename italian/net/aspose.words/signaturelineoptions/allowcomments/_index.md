---
title: SignatureLineOptions.AllowComments
linktitle: AllowComments
articleTitle: AllowComments
second_title: Aspose.Words per .NET
description: Abilita i commenti dei firmatari nella finestra di dialogo Firma con la proprietà AllowComments di SignatureLineOptions. Migliora la collaborazione e il feedback senza sforzo!
type: docs
weight: 20
url: /it/net/aspose.words/signaturelineoptions/allowcomments/
---
## SignatureLineOptions.AllowComments property

Ottiene o imposta un valore che indica che il firmatario può aggiungere commenti nella finestra di dialogo Firma. Il valore predefinito per questa proprietà è`falso` .

```csharp
public bool AllowComments { get; set; }
```

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

* class [SignatureLineOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
