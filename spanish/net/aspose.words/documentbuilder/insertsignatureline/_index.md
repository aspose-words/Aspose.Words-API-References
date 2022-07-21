---
title: InsertSignatureLine
second_title: Referencia de API de Aspose.Words para .NET
description: Inserta una línea de firma en la posición actual.
type: docs
weight: 420
url: /es/net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(SignatureLineOptions) {#insertsignatureline}

Inserta una línea de firma en la posición actual.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | El objeto que almacena los parámetros de creación de la línea de firma. |

### Valor_devuelto

El nodo de línea de firma que se acaba de insertar.

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

* class [Shape](../../../aspose.words.drawing/shape)
* class [SignatureLineOptions](../../signaturelineoptions)
* class [DocumentBuilder](../../documentbuilder)
* espacio de nombres [Aspose.Words](../../documentbuilder)
* asamblea [Aspose.Words](../../../)

---

## InsertSignatureLine(SignatureLineOptions, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, WrapType) {#insertsignatureline_1}

Inserta una línea de firma en la posición especificada.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | El objeto que almacena los parámetros de creación de la línea de firma. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la línea de la firma. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la línea de la firma. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia hasta la línea de la firma. |
| top | Double | Distancia en puntos desde el origen hasta el lado superior de la línea de la firma. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la línea de la firma. |

### Valor_devuelto

El nodo de línea de firma que se acaba de insertar.

### Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el [`Shape`](../../../aspose.words.drawing/shape) objeto devuelto por este método.

### Ejemplos

Muestra cómo insertar una línea de firma en línea en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    Signer = "John Doe",
    SignerTitle = "Manager",
    Email = "johndoe@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, 2.0,
    RelativeVerticalPosition.Page, 3.0, WrapType.Inline);

// La línea de firma se puede firmar en Microsoft Word haciendo doble clic en ella.
doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape)
* class [SignatureLineOptions](../../signaturelineoptions)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* espacio de nombres [Aspose.Words](../../documentbuilder)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
