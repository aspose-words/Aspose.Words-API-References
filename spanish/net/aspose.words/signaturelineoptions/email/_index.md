---
title: SignatureLineOptions.Email
second_title: Referencia de API de Aspose.Words para .NET
description: SignatureLineOptions propiedad. Obtiene o establece la dirección de correo electrónico del firmante sugerido. El valor predeterminado para esta propiedad es cuerda vacía Empty .
type: docs
weight: 40
url: /es/net/aspose.words/signaturelineoptions/email/
---
## SignatureLineOptions.Email property

Obtiene o establece la dirección de correo electrónico del firmante sugerido. El valor predeterminado para esta propiedad es **cuerda vacía** (Empty ).

```csharp
public string Email { get; set; }
```

### Ejemplos

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

// Vuelva a abrir nuestro documento guardado y verifique que las propiedades "IsSigned" y "IsValid" sean iguales a "true",
// indicando que la línea de la firma contiene una firma.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Ver también

* class [SignatureLineOptions](../)
* espacio de nombres [Aspose.Words](../../signaturelineoptions/)
* asamblea [Aspose.Words](../../../)


