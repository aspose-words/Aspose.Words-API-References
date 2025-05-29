---
title: SignatureLineOptions Class
linktitle: SignatureLineOptions
articleTitle: SignatureLineOptions
second_title: Aspose.Words para .NET
description: Descubre Aspose.Words.SignatureLineOptions para personalizar fácilmente las líneas de firma en tus documentos. ¡Mejora tu experiencia con DocumentBuilder hoy mismo!
type: docs
weight: 6940
url: /es/net/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class

Permite especificar opciones para la línea de firma que se inserta. Se utiliza en[`DocumentBuilder`](../documentbuilder/) .

Para obtener más información, visite el[Trabajar con firmas digitales](https://docs.aspose.com/words/net/working-with-digital-signatures/) Artículo de documentación.

```csharp
public class SignatureLineOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [SignatureLineOptions](signaturelineoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowComments](../../aspose.words/signaturelineoptions/allowcomments/) { get; set; } | Obtiene o establece un valor que indica que el firmante puede agregar comentarios en el cuadro de diálogo Firmar. El valor predeterminado para esta propiedad es`FALSO` . |
| [DefaultInstructions](../../aspose.words/signaturelineoptions/defaultinstructions/) { get; set; } | Obtiene o establece un valor que indica que las instrucciones predeterminadas se muestran en el cuadro de diálogo Firmar. El valor predeterminado para esta propiedad es`verdadero` . |
| [Email](../../aspose.words/signaturelineoptions/email/) { get; set; } | Obtiene o establece la dirección de correo electrónico del firmante sugerido. El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |
| [Instructions](../../aspose.words/signaturelineoptions/instructions/) { get; set; } | Obtiene o establece instrucciones para el firmante que se muestran al firmar la línea de firma. El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |
| [ShowDate](../../aspose.words/signaturelineoptions/showdate/) { get; set; } | Obtiene o establece un valor que indica que la fecha de la firma se muestra en la línea de firma. El valor predeterminado para esta propiedad es`verdadero` . |
| [Signer](../../aspose.words/signaturelineoptions/signer/) { get; set; } | Obtiene o establece el firmante sugerido de la línea de firma. El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |
| [SignerTitle](../../aspose.words/signaturelineoptions/signertitle/) { get; set; } | Obtiene o establece el título sugerido del firmante. El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
