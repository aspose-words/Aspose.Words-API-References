---
title: SignatureLineOptions.ShowDate
linktitle: ShowDate
articleTitle: ShowDate
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad SignatureLineOptions ShowDate mejora la profesionalidad de su documento al mostrar la fecha de firma en las líneas de firma.
type: docs
weight: 60
url: /es/net/aspose.words/signaturelineoptions/showdate/
---
## SignatureLineOptions.ShowDate property

Obtiene o establece un valor que indica que la fecha de la firma se muestra en la línea de firma. El valor predeterminado para esta propiedad es`verdadero` .

```csharp
public bool ShowDate { get; set; }
```

## Ejemplos

Muestra cómo firmar un documento con un certificado personal y una línea de firma.

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

// Vuelva a abrir nuestro documento guardado y verifique que las propiedades "IsSigned" e "IsValid" sean ambas iguales a "true",
// indica que la línea de firma contiene una firma.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Ver también

* class [SignatureLineOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
