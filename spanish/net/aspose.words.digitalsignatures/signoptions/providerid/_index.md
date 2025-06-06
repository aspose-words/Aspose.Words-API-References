---
title: SignOptions.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words para .NET
description: Descubra la propiedad SignOptions ProviderId, que define el ID de clase de su proveedor de firma. Personalícela fácilmente con un GUID único para un rendimiento óptimo.
type: docs
weight: 40
url: /es/net/aspose.words.digitalsignatures/signoptions/providerid/
---
## SignOptions.ProviderId property

Especifica el ID de clase del proveedor de firma. El valor predeterminado es**Guía vacía (todos ceros)** .

```csharp
public Guid ProviderId { get; set; }
```

## Observaciones

El proveedor de servicios criptográficos (CSP) es un módulo de software independiente que ejecuta algoritmos criptográficos de autenticación, codificación y cifrado. MS Office reserva el valor {00000000-0000-0000-0000-00000000000} para su proveedor de firmas predeterminado.

El GUID del proveedor instalado adicionalmente debe obtenerse de la documentación enviada con el proveedor.

Además, todos los proveedores criptográficos instalados se enumeran en el registro de Windows. Se puede encontrar en la siguiente ruta: HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Hay un nombre de clave "CP Service UUID" que corresponde a un GUID del proveedor de firma.

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

* class [SignOptions](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)
